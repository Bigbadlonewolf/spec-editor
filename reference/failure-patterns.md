# failure-patterns.md — The Named Failure Patterns

The recurring ways early-stage specs fail. Every finding in a critique must name
one of these patterns (or name a new one precisely — if you cannot name it, you do
not understand it well enough to critique it).

For each pattern: definition, tells, and the mechanism — why it happens to smart
PMs.

---

## 1. Solution-Shaped Problem
The "problem" section is a feature description wearing a trench coat.
**Tells:** the problem statement mentions the product, its features, or the absence
of a feature ("users can't filter by date"); zero user pain described.
**Mechanism:** the PM fell in love with the solution first and reverse-engineered a
problem to justify it. The spec can now never discover the solution is wrong.

## 2. Vibes-Based Evidence
Claims about user demand with no counts, quotes, sources, or links.
**Tells:** "users are asking for this", "we've heard feedback", "everyone knows" —
with nothing attached; a single anecdote presented as a pattern.
**Mechanism:** early-stage PMs absorb founder conviction as if it were user
evidence. The spec inherits the founder's confidence without the founder's context.

## 3. Metric Mirage
Success metrics that cannot be measured, or measure something other than the user
outcome.
**Tells:** "increase engagement"; targets without baselines; no timeframe; metrics
the current analytics stack cannot produce; the metric is a launch/no-launch
decision tool but no one has said who reads it or when.
**Mechanism:** metrics written to make the spec look rigorous rather than to make a
decision. Ask: "what decision does this metric drive, and when?"

## 4. The 14-Item P0
Everything is critical; no tradeoff has actually been made.
**Tells:** more than ~3 P0/MVP items; "P0" lists that read like a full roadmap;
nothing the PM is willing to cut.
**Mechanism:** prioritization is the PM's core job, and it is the first thing that
dies under stakeholder pressure. A spec that protects everything protects nothing —
engineering will now make the tradeoff decision instead of product.

## 5. Ghost Non-Goals
No out-of-scope section; the boundary of the work is undefined.
**Tells:** no non-goals section; or non-goals that are strawmen nobody proposed.
**Mechanism:** scope is defined by exclusion, and exclusions are socially expensive
— someone in the room wanted that thing. The PM avoided the conversation by omitting
the section. Engineering will now have the conversation mid-sprint, at 10x the cost.

## 6. Assumptions in Facts' Clothing
Unvalidated beliefs stated as established truths, with no open-questions section to
catch them.
**Tells:** "users want X" / "customers will pay for Y" stated flatly; zero open
questions anywhere in the document.
**Mechanism:** at early stage, most of what a PM "knows" is hypothesis. Specs that
don't separate knowledge from belief send engineering to build on belief. A spec
with no open questions is not a confident spec — it is a spec whose assumptions are
hiding.

## 7. Happy-Path-Only Requirements
Requirements describe only the golden flow.
**Tells:** no error states, empty states, loading states, permission cases, or
data edge cases; acceptance criteria absent or unverifiable ("works smoothly").
**Mechanism:** happy paths are fun to write and edge cases are tedious — but edge
cases are where early-stage products lose users and where engineering estimates
double. Special alarm: permissions, money, and data-loss paths.

## 8. Jargon Shield
Vagueness hidden behind buzzwords — sounds like a decision, commits to nothing.
**Tells:** "leverage AI to optimize", "seamless experience", "best-in-class",
"robust", "intuitive" — applied to requirements or problem statements.
**Mechanism:** jargon is what ambiguity wears when it wants to look like expertise.
Each buzzword is a question the PM declined to answer. Translate the phrase back
into plain behavior; if it dissolves, it's this pattern.

## 9. No Kill Criteria
No defined condition under which the team stops, shrinks, or pivots the work.
**Tells:** kill/pivot criteria absent, or so loose nothing could trigger them.
**Mechanism:** early-stage companies die from opportunity cost, not from one bad
feature. Sunk cost is the strongest force in a small team; kill criteria defined
*before* the build are the only reliable counterweight.

## 10. Stakeholder Silence
No signal that engineering or design has pressure-tested the approach, and no
dependencies called out.
**Tells:** a spec heading to engineering with no record of engineering input;
third-party APIs, data availability, or other teams assumed without verification.
**Mechanism:** solo PMs write in a vacuum to move fast, and accidentally commit
engineering to an approach they've never seen. The first technical objection then
arrives after the team has emotionally committed to the plan.

## 11. Stage Confusion
Process weight mismatched to company stage.
**Tells:** six-week discovery phases, four stakeholder sign-offs, or FAANG-style
PRD templates on a five-person team — or conversely, a napkin spec at Series A
where compliance, enterprise customers, or a 15-person eng org now exist.
**Mechanism:** PMs import process from the last company or from content written
for big-company PMs. Process is a tool, not a virtue; the right amount is a
function of blast radius and team size.

## 12. Timeline Fiction
Dates with no milestones, sequencing rationale, or stated assumptions.
**Tells:** a launch date with no phases; every milestone dependent on nothing going
wrong; dates that exist because a founder asked for one.
**Mechanism:** dates without rationale are negotiation artifacts, not plans. They
erode PM credibility the first time they slip — and they always slip.

## 13. Automation Without a Floor
An AI/ML feature spec with no quality floor: nothing defines good-enough output,
cold-start behavior, or what happens when the model is wrong.
**Tells:** "AI-powered X" with no eval criteria or quality bar; no answer to "what
does it do on day one, before any data exists?"; no stated behavior for bad output
(fallback, human review path, confidence display); success metrics about engagement
with the feature but none about the quality of its output.
**Mechanism:** the PM spec'd the capability, not the trust. Automation features
don't fail by not working — they fail by working badly just often enough to erode
user trust in the whole product, and by then the habit of checking is gone. The
floor is the feature.

---

## If a weakness matches no pattern above

Name it yourself, precisely, in the same style: what it is, its tell, its
mechanism. A named failure is teachable; an unnamed vibe is not critique.
