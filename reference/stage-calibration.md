# stage-calibration.md — Rigor Is a Function of Stage

The same spec deserves different critique at different stages. Your job is to
apply the *right* ruler — demanding Series A process from a pre-seed team is as
much an editorial failure as accepting napkin rigor at Series A.

If stage cannot be determined from the spec or the writer's message, **assume
pre-seed, say so in one line, and invite correction.**

---

## Pre-seed (team: ~2–8 people, PM often = founder or first hire)

**The scarce resource is learning speed, and the existential risk is building
the wrong thing at all.**

| Section | Right-sized expectation |
|---|---|
| Problem | Sharp, solution-free, one paragraph. |
| Evidence | 5–10 real user conversations, support patterns, or founder-led sales notes beat any survey. Counts and quotes, not decks. |
| Metrics | One metric that matters, a baseline, and a "we'll check at week N." Instrumentation plans are cargo cult here. |
| Scope | Ruthless. Non-goals mandatory. MVP = days-to-few-weeks of work. |
| Requirements | Happy path + the 2–3 edges that can kill you (permissions, money, data loss). Exhaustive edge-case catalogs are waste. |
| Dependencies | A hallway conversation with the engineer, noted in one line. |
| Kill criteria | **Mandatory.** This is the stage where opportunity cost kills. |
| Milestones | Three bullets: what ships, when we check, what we learn. |

**Where specs at this stage most often fail:** evidence quality, problem shape,
scope discipline, and kill criteria. Formatting, templates, and thin process are
non-issues here.

---

## Seed (team: ~8–20 people, eng team 4–8, first real handoffs happening)

**The scarce resource is engineering coordination; the new risk is the spec as a
communication artifact, not just a thinking artifact.**

| Section | Right-sized expectation |
|---|---|
| Problem + Evidence | As pre-seed, plus baselines where analytics exist. |
| Metrics | Baseline + target + timeframe + who checks. Lightweight instrumentation is now fair to demand. |
| Scope | Non-goals mandatory; P0 ≤ 3 items with explicit cut-line rationale. |
| Requirements | Happy path + error/empty/permission states for core flows. Acceptance criteria become verifiable. |
| Dependencies | Engineering and design have seen it *before* handoff; third-party and data dependencies verified, not assumed. |
| Kill criteria | Still mandatory. |
| Milestones | Phased ship plan; riskiest assumption validated earliest. |

**Where specs at this stage most often fail:** all pre-seed failure modes, plus
handoff quality — edge cases, dependency verification, and engineering pressure-
testing before handoff.

---

## Series A (team: ~20–60, eng 10–20+, possibly enterprise customers or
regulated context)

**The new risks are blast radius and cross-functional alignment. A bad spec now
costs quarters, not sprints, and can create contractual or compliance exposure.**

| Section | Right-sized expectation |
|---|---|
| Evidence | Quantified: funnels, cohort data, churn analysis alongside qualitative. |
| Metrics | Instrumentation plan is now a legitimate demand; metric ownership named. |
| Scope | Non-goals + explicit tradeoff narrative (what was cut and why). |
| Requirements | Full edge-case coverage incl. failure modes; acceptance criteria testable by QA that isn't the PM. |
| Dependencies | Cross-team sign-off where blast radius crosses teams; security/legal/compliance review where regulated or contractual. |
| Kill criteria | May fold into launch gates / rollout plan (feature flags, staged rollout, rollback plan) rather than a standalone section. |
| Milestones | Sequencing rationale + rollout plan; dates may carry external commitments. |

**Where specs at this stage most often fail:** all earlier failure modes, plus
blast radius — rollout, rollback, cross-team dependencies, and reviewability by
people who weren't in the room.

---

## Anti-patterns of calibration (do not do these)

- **Importing big-co process downward:** demanding instrumentation plans,
  RACI charts, or multi-week discovery from a 5-person team. This is Stage
  Confusion committed by the *editor* — the worst version of the sin.
- **Forgiving upward:** accepting founder-conviction-as-evidence at Series A.
  What was charming scrappiness at pre-seed is negligence at Series A.
- **Grading the template, not the thinking:** a beautiful PRD template with
  hollow sections fails; three sharp paragraphs with real evidence can pass at
  pre-seed.
