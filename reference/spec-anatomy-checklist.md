# spec-anatomy-checklist.md — The Load-Bearing Sections

The skeleton of a spec that an early-stage engineering team can build from.
Use this to detect **missing sections** and **hollow sections** (heading present,
thinking absent — a hollow section is usually more dangerous than a missing one
because it creates false confidence).

Not every spec needs every section at equal depth — depth is calibrated by stage
(see `stage-calibration.md`). But a section that is *relevant and absent* is a
finding; a section that is *present and hollow* is usually a bigger one.

---

## 1. Problem statement
The user pain, stated without mentioning the product or its features.
**Hollow tells:** the "problem" describes a missing feature ("users can't do X in
our app") rather than a user pain; no evidence of who hurts, how often, or what it
costs them.

## 2. Evidence
Why the writer believes the problem is real: user interviews, support tickets,
usage data, churn exit notes, sales-lost reasons — with counts, quotes, or links.
**Hollow tells:** "users are asking for this" with no source; evidence section that
is one anecdote; evidence that is actually market-size slides (TAM is not problem
evidence).

## 3. User & context
Which specific user segment hurts, and in what moment of their workflow.
**Hollow tells:** "all users"; persona names without behavior; no description of
what the user does today instead (the workaround is the real competitor).

## 4. Success metrics
A measurable definition of done: metric, baseline, target, timeframe, and how it
will be measured.
**Hollow tells:** "increase engagement"; targets with no baseline; metrics the
team cannot currently measure; no timeframe; no statement of what happens if the
target is missed.

## 5. Scope & non-goals
What this spec covers — and an explicit list of what it does **not** cover.
**Hollow tells:** no non-goals section at all; non-goals that are strawmen
("we won't rebuild the whole app"); a P0 list long enough to be a roadmap.

## 6. Requirements
Functional requirements an engineer can implement and a reviewer can verify —
including error states, empty states, loading states, permissions, and data edge
cases.
**Hollow tells:** requirements that describe UI but not behavior; only the happy
path; "it should just work" phrasing; acceptance criteria absent or unverifiable
("works well", "feels fast").

## 7. Dependencies & risks
What must be true for this to work: other teams, third-party APIs, data
availability, technical constraints, and a signal that engineering/design has
seen and pressure-tested the approach.
**Hollow tells:** no mention of engineering input on a spec heading to
engineering; risks section listing only schedule risks, never "this might be the
wrong thing."

## 8. Open questions
Explicit unknowns, owned and named — the spec's honest admission of what is
not yet decided.
**Hollow tells:** no open questions section (a spec with no open questions at
early stage is a spec whose assumptions are hiding); questions listed with no
owner or resolution path.

## 9. Kill / pivot criteria
What result would make the team stop, shrink, or redirect this work — defined
before the build, while judgment is still cheap.
**Hollow tells:** absent entirely (most common); criteria so loose nothing could
trigger them ("if it doesn't go well").

## 10. Milestones (stage-dependent)
Phasing: what ships first, what validates the riskiest assumption earliest.
At pre-seed this can be three bullets; at Series A it should include sequencing
rationale. **Hollow tells:** dates with no rationale; a single "launch" milestone
for multi-week work.

---

## About this file

This file is the editor's diagnostic instrument for detecting missing and hollow
sections: it catalogs the load-bearing sections and the ways each one goes hollow.
It is not a compliance form — it does not prescribe that every spec contain every
section. Which absences create real risk depends on company stage (see
`stage-calibration.md`) and is adjudicated by the severity rules in `rules.md`.
