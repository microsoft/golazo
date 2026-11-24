# Golazo Overview – Full Narration Script (≈10 Minutes)

_This script has been edited for reading. It isn't a verbatim transcript of the video._

## Hook & Pain Framing

Picture a pull request that's been waiting all week. A reviewer finally opens it and asks whether
the team should take a different approach. Now the author has to redo work they thought was done.

I'll show you how Golazo brings that conversation forward and helps teammates see where they can
help finish work.

## What Is Golazo

Golazo is a way for small and midsize engineering teams to organize their work. Think four to ten
engineers. Work in small pieces, make it easy to see how each ticket is doing, and check that the
change helped before calling it done.

Here's what the team uses:

1. Small tickets with an outcome someone can check.
2. Short design docs that two peers sign off on.
3. A board that shows where each ticket is and which work takes priority.
4. Standups, retrospectives, and planning to unblock work and decide what to do next.

Agree on the approach, build a small change, review it, and check that it worked.

## Mapping Pains to Practices

- If reviewers keep asking for a different design, use the design doc to discuss it before coding.
- If feedback comes late, deliver a smaller change and show on the board where it's waiting.
- If only one person knows an area, someone else can pull a Ready ticket there, pair with them, and
  read past design docs.
- If everyone is juggling tickets, limit work in progress so they can finish one.
- If a merged change still hasn't fixed the problem, customer validation gives the team a chance to
  find that out before closing the ticket.
- If standup is just a status report, ask what the team learned and what would move each ticket
  forward.

## Design Docs (Core Mechanism)

Keep the design doc short. Explain the problem, the goal, the constraints, the approach, and the
work it will take.

Ask two peers to sign off before you start. They can leave questions in the doc, where there's still
time to change the plan. Keep the doc after the ticket is done so the next person can find out why
you chose that approach.

## Task Board & Priority Rails

Look at the task board to see what's waiting for a review, what's blocked, and what needs help.

The columns show how far a ticket has come. An idea starts in Backlog. Once it's Ready, an engineer
can pull it without waiting for someone to assign it. The ticket goes through design, engineering,
release, and validation before it reaches Done.

The rails show priority. Use Swarm for urgent work that needs the team's attention, Interrupt for
unexpected work that can't wait for the usual queue, and Planned for work the team picked ahead of
time.

## WIP Limits & Flow

When you hit a work-in-progress limit, help finish a ticket before pulling another. If tickets are
piling up in review, you might be able to review one. With fewer things in progress, it's also
easier to help when an incident needs a Swarm.

## Small Tickets & Slicing

Before pulling a ticket, ask: What will a user get from this? Can we build it in under two weeks?
How will we check that it helped? Is anything blocking us from starting?

For a larger feature, find a piece someone can try on its own. Use that feedback to decide what to
build next.

## Integrated Review & Knowledge Spread

Link the design doc in the pull request so reviewers can see what the team agreed on. They can focus
on whether the code works and which cases it might miss. That context also helps someone review code
outside their usual area.

## Customer Validation Stage

Once the code is merged, check whether the change did what you intended. Ask a stakeholder to try
it, check whether people are using it, or see if the metric you expected to change has moved.
Feedback from a pilot or your own team's use of the feature can help too. If the check fails, move
the ticket backward so the remaining work is visible.

## Team Morale

Picking up an unfamiliar ticket is easier when you know who to ask for help. Spend 15 minutes
looking at an edge case together, or ask someone to read a design choice before you code it. Use
shared channels so anyone with an answer can join in. If nobody responds or a ticket slips, find out
what support the team can offer.

## Closing & Call to Action

When the team misses an edge case, ask where you could have caught it: in design, in review, or when
testing the release. Then decide together what to change next time.

Start with "Why Golazo" for more examples of the problems these practices are meant to solve.
