# Templates and Examples

## Design Doc Template

```
# Title

## Elevator Pitch
(What value, for whom, why now)
TODO

## Definition of Done
(Bulleted list describing the exit criteria and desired end state. Should be clear how success is determined and measured)
- TODO

## Customer / Consumer
(Who will be consuming this work? Who will validate that it is correct?)
- TODO

## Dependencies
(Key/major people or technology)
- TODO

## Assumptions / Out of Scope
(Assumptions when planning the ticket and/or related work that is not in scope for this ticket)
- TODO

## Design and Testing Approach
(Free text/diagram/picture/etc that clearly shows your approach and considerations)
- TODO

## Task List
(Bulleted list of engineering work, documentation, monitors, TSGs, etc. Engineering will be complete when the list is finished.)
- [ ] Implementation
- [ ] Tests
- [ ] Monitoring / Metrics
- [ ] Documentation

## Estimated Completion
(You have 95% confidence that teh work will be completed by this date barring any enormous disaster.)
- YYYY-MM-DD

## Signoffs
- Reviewer 1: (Name / Date)
- Reviewer 2: (Name / Date)

## Implementation Notes
(Optional place to include key learnings, decisions, discoveries, data sources, contact information, etc)
TODO
```

## Ticket Sizing Checklist

Use before pulling a ticket from Ready or when splitting.

- Delivers standalone, demonstrable value (stakeholder can say ✅ / ❌).
- Fits within SLA (less than 2 weeks, ideally a few days).
- Acceptance criteria are concrete and testable.
- Quality signals (tests, monitoring, docs) identified.
- Design complexity understood or a spike precedes it.
- Dependencies known and minimal; external waiting minimized.
- Can be shepherded by a single person (pairing allowed) without being blocked on others.

---

## Example Design Doc (Filled)

Below is a realistic example using the template for a small, high‑value improvement. It demonstrates
lean structure, explicit quality signals, and alignment with Golazo principles (deliver quickly,
build quality in, create knowledge, optimize the whole).

```
# Title
Server‑Side Read Cache for Product Catalog Endpoints

## Elevator Pitch
Frequent unauthenticated requests for the product catalog (top sellers, categories, daily deals) account for ~42% of API traffic and create avoidable database load and p95 latency (~420ms). Introducing a lightweight server‑side cache using Azure Cache for Redis in front of .NET 8 minimal API endpoints will cut average response times, reduce Azure SQL read pressure, and improve user perceived performance. This is valuable now because traffic is seasonally spiking and latency‑sensitive features (personalized deals) are preparing to launch.

## Definition of Done
- Cache layer in front of existing read endpoints: /catalog/top, /catalog/categories, /catalog/deals
- Cache TTLs tuned: top (300s), categories (3600s), deals (120s)
- Cache hit ratio >= 70% after first warm period (24h) with monitoring dashboard
- Feature can be toggled off/on via config flag without redeploy

## Customer / Consumer
- External users (faster perceived load times)
- Internal stakeholders: Product Owner validates latency and experience

## Dependencies
- Azure Cache for Redis (existing Enterprise cluster capacity confirmed with SRE: <5% projected memory increase)
- Application Insights / Azure Monitor (SDK already integrated; adding custom metrics + Kusto queries)
- Azure API Management (exposure layer; feature flag passed via configuration)

## Assumptions / Out of Scope
- Write‑path optimizations (separate ticket if needed)
- No per‑user personalization in cache entries (future extension)
- Staleness within TTL acceptable; business rules do not require real‑time updates
- Multi‑region active/active routing handled by traffic manager (cache consistency not cross‑region for now)

## Design and Testing Approach
High‑level flow:

Client -> API Handler -> CacheLookup(key) ->
	Hit: return cached payload
	Miss: acquire single‑flight lock -> DB queries -> hydrate response -> store -> release -> return

Key Points:
- Keys namespaced (catalog:top, catalog:categories, catalog:deals) to avoid collisions.
- Single‑flight (in‑process mutex + short lock TTL fallback) prevents thundering herd (using a memory cache + RedLock fallback only if needed for distributed coordination later).
- Serialization: JSON stored directly; payload size avg <25KB (validated from sample Query + Azure Application Insights sampling).
- Observability: OpenTelemetry + Application Insights exporter wrap cache operations (dependency telemetry + custom metrics).
- Warm strategy: first 10 requests naturally populate; no pre‑warm complexity.
- Failure mode: if Azure Cache unavailable, system logs warning, emits dependency failure metric, and transparently falls back to Azure SQL (circuit breaker after 5 consecutive connection failures to reduce repeated attempts).
- Load test with Azure Load Testing (1k RPS mixed distribution) verifies latency improvements and observes hit ratio after initial warm.

Risk Mitigations:
- Stampede -> Single‑flight lock & short TTL choices
- Memory growth -> Sample average size * expected key count fits comfortably (<50MB) in Azure Cache for Redis
- Silent degradation -> Alerts for miss surge & Azure Cache dependency failures (Application Insights Kusto query + alert rule)
- Regional outage -> Falls back to DB + feature flag toggle via Azure App Configuration

## Task List
- [ ] Baseline metrics capture (current p95, QPS, payload sizes)
- [ ] Define cache key & TTL constants
-- [ ] Implement cache client wrapper + health check (Azure Cache for Redis .NET client)
- [ ] Add single‑flight guard
- [ ] Integrate endpoints (top, categories, deals)
- [ ] Unit tests (key generation, TTL logic, fallback behavior)
- [ ] Integration tests (cold then warm sequence, forced Redis failure)
- [ ] Load test & record results (attach summary)
-- [ ] Observability: custom metrics (hit/miss, evictions), dependency telemetry, dashboard workbook, Azure Monitor alert rule
- [ ] Documentation updates (README + runbook + TSG)
- [ ] Config flag & validation in staging
- [ ] Production rollout & post‑launch metrics review

## Estimated Completion
2025-11-14

## Signoffs
- Reviewer 1: TBD (Date)
- Reviewer 2: TBD (Date)

## Implementation Notes
- Baseline p95 (2025-11-03, Kusto query in Application Insights) collected: top=420ms, categories=390ms, deals=450ms.
- Initial Azure Load Testing prototype showed 68% hit ratio with default TTLs; tuning deals TTL from 60s to 120s projected to exceed 70%.
- Consider future enhancement: background refresh (async refresh just before expiry) using Azure Functions timer trigger.
- Azure Cache for Redis connection pool sized (max 50); estimated peak concurrent cache ops ~20.
- If hit ratio <50% after 24h, investigate key churn (possibly dynamic deals query parameters) and consider normalizing inputs; Kusto workbook slice by key.
```
