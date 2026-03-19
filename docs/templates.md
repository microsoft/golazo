# Templates and Examples

## Design Doc Template

Use this template as a starting point. The goal is to capture enough information to align the team,
not to produce a polished specification.

```
# Title

## Elevator Pitch
(What value is being delivered, for whom, and why now?)
TODO

## Definition of Done
(List the conditions that must be true before the work can be considered complete.)
- TODO

## Customer / Consumer
(Who is affected by the work, and who will validate it?)
- TODO

## Dependencies
(Important people, systems, services, or external conditions.)
- TODO

## Assumptions / Out of Scope
(Assumptions being made and adjacent work that is intentionally excluded.)
- TODO

## Design and Testing Approach
(Describe the intended approach clearly enough that peers can review it.)
- TODO

## Task List
(List the implementation, test, monitoring, documentation, and rollout work.)
- [ ] Implementation
- [ ] Tests
- [ ] Monitoring / Metrics
- [ ] Documentation

## Estimated Completion
(A high-confidence date, not a best-case guess.)
- YYYY-MM-DD

## Signoffs
- Reviewer 1: (Name / Date)
- Reviewer 2: (Name / Date)

## Implementation Notes
(Optional notes about discoveries, follow-up work, or references.)
TODO
```

## Ticket Sizing Checklist

Use this checklist before pulling a ticket from Ready or when deciding whether to split it.

- The ticket delivers a standalone outcome that someone can validate.
- The scope fits within the team SLA.
- Acceptance criteria are specific enough to test.
- Required quality work such as tests, monitoring, and documentation is understood.
- The design complexity is known well enough, or a spike exists to reduce uncertainty.
- Dependencies are limited enough that the ticket is not mostly waiting.
- One shepherd can keep the ticket moving even if the implementation is paired.

---

## Example Design Doc (Filled)

This example is intentionally concise. It shows the level of detail needed for a small but real
engineering improvement without turning the document into an essay.

```
# Title
Server-Side Read Cache for Product Catalog Endpoints

## Elevator Pitch
Unauthenticated catalog requests currently account for about 42% of API traffic and are creating unnecessary database load. Recent telemetry shows p95 latency between 390 ms and 450 ms across the highest-volume read endpoints. This change introduces a lightweight server-side cache in front of those endpoints to reduce read pressure and improve response time before the next seasonal traffic increase.

## Definition of Done
- A cache layer exists for `/catalog/top`, `/catalog/categories`, and `/catalog/deals`
- Initial TTLs are set to 300s, 3600s, and 120s respectively
- Cache hit ratio is at least 70% after 24 hours of steady production traffic
- The cache can be disabled through configuration without redeployment

## Customer / Consumer
- External users consuming catalog endpoints
- Product owner validating latency and overall user experience

## Dependencies
- Existing Azure Cache for Redis cluster with confirmed spare capacity
- Application Insights and Azure Monitor for telemetry and alerting
- API Management configuration path for rollout and feature control

## Assumptions / Out of Scope
- Write-path optimization is not included
- Per-user personalization is not part of the cache key design
- A small amount of staleness within the TTL window is acceptable
- Cross-region cache consistency is not required for the first version

## Design and Testing Approach
Request flow:

Client -> API handler -> cache lookup -> hit returns cached payload
Client -> API handler -> cache lookup -> miss reads from database, stores result, returns payload

Notes:
- Cache keys are namespaced by endpoint
- A single-flight guard is used to reduce duplicate load on misses
- Payloads are stored as JSON without extra transformation layers
- Cache operations emit dependency telemetry plus hit and miss counters
- If Redis is unavailable, the API falls back to the database and records the failure
- Load testing is used to validate latency improvement and warm-cache behavior

## Task List
- [ ] Capture baseline latency and traffic metrics
- [ ] Define cache keys and TTL constants
- [ ] Implement cache wrapper and health check
- [ ] Add single-flight guard for misses
- [ ] Integrate the three target endpoints
- [ ] Add unit tests for key generation, TTL logic, and fallback behavior
- [ ] Add integration tests for cold cache, warm cache, and Redis failure
- [ ] Run load test and attach summary
- [ ] Add dashboard, hit or miss metrics, and alert rules

## Estimated Completion
- 2025-11-14

## Signoffs
- Reviewer 1: TBD (Date)
- Reviewer 2: TBD (Date)

## Implementation Notes
- Baseline p95 on 2025-11-03 was 420 ms for `top`, 390 ms for `categories`, and 450 ms for `deals`
- An early prototype reached 68% cache hit ratio before TTL tuning
- Background refresh is a possible follow-up if miss spikes remain high
- Current connection pool sizing appears sufficient for projected peak load
```
