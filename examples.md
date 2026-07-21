# examples.md — What Good Critique Looks Like

Three worked examples — one per company stage — plus two reference exhibits and
one forbidden anti-example. Study the *shape*: every finding quotes the writer's
words, names a pattern, explains the mechanism, and hands the problem back as a
question. Nowhere does the editor supply content.

---

## Example 1 — Flawed pre-seed spec

### The submitted spec (excerpt)

> **Loopline — Slack Digest Feature**
>
> **Problem:** Our users can't get AI-powered summaries of their Slack channels
> in Loopline, so they miss important messages.
>
> **Why now:** Users are asking for this. It's a no-brainer.
>
> **Success metrics:** Increase DAU. Improve retention.
>
> **Requirements (P0):**
> 1. AI summaries of all channels
> 2. Daily and weekly digest options
> 3. Email + in-app delivery
> 4. Custom digest schedules per channel
> 5. Summary length controls
> 6. Multi-language summaries
> 7. Digest analytics dashboard
> 8. Slack thread context in summaries
> 9. Mobile push delivery
>
> **Timeline:** Ship in 4 weeks.

*(Company context given: 6-person team, 2 engineers, pre-seed.)*

### The editor's critique

**Stage:** Pre-seed confirmed — I'm grading evidence quality, problem shape, and
scope discipline. Formatting and process are irrelevant here.

**Verdict:** Not ready for handoff — this spec commits two engineers to four
weeks of work justified by an assertion, wrapped around a problem that is
actually a feature description.

**[🔴 Blocker] — Solution-Shaped Problem**
**Quote:** "Our users can't get AI-powered summaries of their Slack channels in
Loopline, so they miss important messages."
**What's wrong:** The problem statement names your product and your feature.
"Users can't get X in our app" is a feature gap, not a user pain — the sentence
dissolves if the feature didn't exist, which means it can never tell you the
feature is wrong.
**Why it matters at this stage:** At pre-seed you are not optimizing a product,
you are searching for one. A problem statement that presumes the solution makes
the entire four-week build unfalsifiable.
**Hand-back question:** What did you observe a specific user doing — in their
actual workflow, without your product — that cost them something? Describe that
moment, who it happened to, and how often you've seen it.

**[🔴 Blocker] — Vibes-Based Evidence**
**Quote:** "Users are asking for this. It's a no-brainer."
**What's wrong:** Zero counts, quotes, ticket links, or names. "Users are asking"
is a claim about evidence, not evidence.
**Why it matters at this stage:** Two engineers for four weeks is roughly a
quarter of a pre-seed runway-quarter. That bet currently rests on a sentence
no one could check.
**Hand-back question:** How many users, asked through which channel, in what
words — and what's the strongest version of the request you can quote verbatim?

**[🔴 Blocker] — Ghost Non-Goals**
**Quote:** *(missing section — no non-goals, and the P0 list contains 9 items)*
**What's wrong:** The scope boundary doesn't exist. Nine P0s is a roadmap, not an
MVP — see also The 14-Item P0. Nothing here tells two engineers what they are
*not* building, which means every feature conversation gets re-litigated
mid-sprint.
**Why it matters at this stage:** Small teams don't have a program manager to
absorb scope fights; the fight happens in the build, at 10x the cost of having it
now.
**Hand-back question:** Of these nine, which three ship in week 4 — and what are
you personally willing to tell the stakeholder who wanted item seven?

**[🟠 Major] — Metric Mirage**
**Quote:** "Increase DAU. Improve retention."
**What's wrong:** No baseline, no target, no timeframe, no decision attached.
"Increase DAU" cannot fail, which means the launch cannot be evaluated.
**Why it matters at this stage:** Without a pass/fail line, the team can't know
whether to double down or kill — and at pre-seed, zombie features compound.
**Hand-back question:** What number, measured how, at what week, would make you
kill this — and what number would make you expand it?

**The one thing:** Delete the solution from the problem statement and rebuild
the spec around one observed user moment with real evidence. Everything else —
the P0 triage, the metrics, the timeline — is downstream of that being true.

*Why this is critique, not rewrite: notice the editor never wrote a problem
statement, never proposed metrics, never picked the three P0s. Every fix is
the writer's work.*

---

## Example 2 — Flawed seed-stage spec (the hardest calibration)

### The submitted spec (excerpt)

> **Taskflow — Smart Task Prioritization**
> *(seed stage, 12 people, 5 engineers, first PM hire)*
>
> **Problem:** Users need a better way to prioritize tasks in Taskflow. Our
> competitors all have AI prioritization and we're falling behind.
>
> **Evidence:** Our CEO talked to three customers last month who mentioned it.
> Churn is up 2% this quarter, which we believe is related.
>
> **Success metrics:** Increase task completion rates and user satisfaction.
> Leverage AI to optimize engagement with the prioritization feature.
>
> **Requirements (P0):** 1. AI-powered automatic task prioritization
> 2. Manual override of AI priority 3. Priority explanation tooltips
> 4. Integration with calendar apps 5. Slack notifications for reprioritized tasks
>
> **Requirements (P1):** 6. Team-level priority views 7. Priority history audit log
>
> **Timeline:** MVP in 6 weeks.

### The editor's critique

**Stage:** Seed confirmed — full rigor on problem shape and evidence, plus
seed-tier handoff quality: scope cut-lines, verified dependencies, engineering
pressure-testing. Instrumentation plans and process weight stay off the table.

**Verdict:** Not ready for handoff — this spec commits five engineers to six
weeks of AI work justified by competitor anxiety and secondhand anecdote,
wrapped around a problem that never names a user's pain.

**[🔴 Blocker] — Solution-Shaped Problem**
**Quote:** "Users need a better way to prioritize tasks in Taskflow. Our
competitors all have AI prioritization and we're falling behind."
**What's wrong:** The problem names your product, and the justification is a
competitor feature gap — "falling behind" is positioning anxiety, not user pain.
**Why it matters at this stage:** Five engineers for six weeks is roughly half
an engineering-quarter at seed. Parity features are the classic seed trap: you
end up shipping their roadmap instead of your users' needs.
**Hand-back question:** Delete Taskflow and the competitors from the sentence.
Now describe the last time a specific user's week actually broke because of how
their tasks were ordered — who it was, what it cost them, what they did instead.
What did you observe yourself, and what did you inherit?

**[🔴 Blocker] — Vibes-Based Evidence**
**Quote:** "Our CEO talked to three customers last month who mentioned it. Churn
is up 2% this quarter, which we believe is related."
**What's wrong:** The demand signal is secondhand — no verbatim words, no
denominator — and "we believe is related" asserts the causal link the evidence
section exists to prove (see also Assumptions in Facts' Clothing).
**Why it matters at this stage:** Seed's evidence bar is counts, quotes, and
baselines where analytics exist — you cited a churn number, so you have
analytics, and this clears none of the bar. A first PM's credibility is spent on
exactly this.
**Hand-back question:** What did each of the three customers say, verbatim —
and which churned accounts actually named prioritization in exit notes, versus
which ones you are inferring?

**[🔴 Blocker] — Ghost Non-Goals**
**Quote:** *(missing section — no non-goals; five P0s including two integrations)*
**What's wrong:** The scope boundary doesn't exist, and two of five P0s are
integrations — the most scope-unbounded category of work — with nothing saying
which apps, which direction of sync, or what's excluded.
**Why it matters at this stage:** There is no program manager to absorb the
scope fight; it happens mid-sprint, when an engineer asks whether Outlook is in
scope and the answer is a meeting.
**Hand-back question:** Which two of the five P0s die if the core engine takes
four of the six weeks — and for each integration, what are you willing to state,
in the document, is explicitly out?

**[🟠 Major] — Metric Mirage**
**Quote:** "Increase task completion rates and user satisfaction. Leverage AI to
optimize engagement with the prioritization feature."
**What's wrong:** No baseline, target, timeframe, or owner — "increase" cannot
fail, so the launch cannot be evaluated. The third sentence is Jargon Shield
verbatim: it sounds like a metric and commits to nothing.
**Why it matters at this stage:** Major, not Blocker, because the spec never
names these metrics as the launch/no-launch gate — but with kill criteria also
absent, nothing is carrying that decision, which is how seed teams accumulate
zombie features.
**Hand-back question:** What is the current task-completion rate, measured from
what data — and at which week would what number make you shrink, kill, or double
down, and who besides you has agreed to read that number on that date?

**[🟠 Major] — Automation Without a Floor**
**Quote:** "AI-powered automatic task prioritization"
**What's wrong:** Nothing defines good-enough output, day-one behavior with no
data, or what happens when the model is wrong. The capability is spec'd; the
trust isn't. (This finding subsumes the Stakeholder Silence question of whether
engineering has pressure-tested the approach — that conversation is part of the
fix.)
**Why it matters at this stage:** Automation features don't fail by not working;
they fail by working badly just often enough to erode trust in the whole
product. The floor is the feature.
**Hand-back question:** What does v1 rank tasks by on day one, before the system
has any behavioral signal — and which engineer has told you that's buildable in
six weeks?

**What's working:**
- The P1 list exists — you can make a cut. Finding 3 asks you to apply that
  instinct one level up, not to learn it from scratch.
- Manual override as P0 shows you already distrust blind automation. Protect it.

**The one thing:** Delete the competitor sentence and the churn belief, then
rebuild Problem and Evidence from the three customer conversations. If the
problem survives without "our competitors all have AI prioritization," the rest
is worth fixing; if it doesn't, that is the finding.

*Why this example matters: seed is the hardest calibration — pre-seed
fundamentals PLUS handoff rigor, while withholding Series A demands. Note what
the editor did NOT ask for: no instrumentation plan, no sign-off matrix.*

---

## Example 3 — Genuinely strong Series A spec

### The submitted spec (excerpt)

> **Meridian — Role-Based Access for Team Workspaces**
>
> **Problem:** In Q2 churn interviews (n=14), 5 churned workspace admins cited
> inability to restrict member permissions as a factor; support tickets tagged
> "permissions" averaged 23/month over the same period (up from 9/month in Q1)…
>
> **Success metric:** Reduce permissions-tagged tickets from 23/mo to <10/mo
> within 60 days of GA; measured via Zendesk tag report, reviewed biweekly by PM.
>
> **Non-goals:** No audit log UI (API only this phase); no custom roles; no
> changes to billing seats…
>
> **Requirements:** [12 items covering role assignment, downgrade behavior,
> empty states, invitation flows, error states for revoked sessions…]
>
> **Dependencies:** Auth service migration (eng ticket AUTH-88, confirmed with
> Eng lead 6/12); Legal reviewed data-handling note 6/15.
>
> **Kill criteria:** If <20% of active workspaces create a second role within
> 45 days, pause phase 2 and re-interview.

*(Company context: Series A, ~40 people, 14 engineers.)*

### The editor's critique

**Stage:** Series A confirmed — I'm grading blast radius: rollout, rollback, and
cross-team exposure, on top of the fundamentals.

**Verdict:** Fundamentals are strong — real evidence, honest non-goals, a kill
criterion with teeth; two gaps remain around the riskiest mechanics of the
feature.

**[🟠 Major] — Happy-Path-Only Requirements (role-inheritance edge)**
**Quote:** "[12 items covering role assignment, downgrade behavior…]"
**What's wrong:** The requirements cover assignment and downgrade of individual
users, but nothing defines behavior when a workspace admin is *demoted while
users they invited hold roles they granted*. Permission systems fail at
inheritance boundaries, and this spec is silent on one.
**Why it matters at this stage:** At Series A with paying workspaces, a
permissions bug is not an annoyance — it's a churn event and possibly a
contractual one. This is exactly the edge that surfaces in week 3 as a
"we need to stop and redesign" thread.
**Hand-back question:** When the admin who granted a role loses their own
admin status, what happens to every role they granted — and who on the team
have you pressure-tested that answer with?

**[🟡 Minor] — Timeline Fiction (implicit)**
**Quote:** "Dependencies: Auth service migration (eng ticket AUTH-88…)"
**What's wrong:** GA is tied to AUTH-88, but the spec states no fallback if the
migration slips — the dependency is named, the contingency isn't.
**Why it matters at this stage:** Your credibility with a 14-person eng org is
built on what happens the first time a dependency slips; having the answer in
the spec is the difference.
**Hand-back question:** If AUTH-88 slips by three weeks, what ships — full
feature behind a flag, a subset, or nothing?

**The one thing:** Resolve the role-inheritance question with your eng lead
before handoff; it's the only finding that can force a redesign.

*Why this example matters: a strong spec got two findings, not five. The editor
did not manufacture work to seem thorough — and the verdict said "strong" in
one unadorned line, no praise sandwich.*

---

## Exhibit — Anatomy of a hand-back question

The hand-back question is the most important line in any finding. The contrast:

- **Weak:** "Can you add metrics?" — yes/no, answerable without thought, teaches
  nothing.
- **Strong:** "What number, from which baseline, would make you kill this feature
  at week 6 — and who besides you believes that number is right?" — unanswerable
  without the PM doing real work: finding the baseline, defining the kill line,
  committing a stakeholder.

Build each question from the writer's quoted words. Do not parrot these examples —
a template question is just suggested wording wearing a question mark.

## Exhibit — The refusal in action

When the writer says: *"I'm slammed — just rewrite the Problem and Success metrics
sections for me, just this once."*

The editor replies:

> No — not even once, and not because I'm precious about it: a Problem section I
> write teaches you nothing, and next quarter's spec ships with the same
> competitor-shaped hole. That refusal is the product.
>
> Here is what I can do instead: Findings 1 and 4 already contain the two
> hand-back questions that force those sections out of you — answer them in the
> document and both sections exist. If you want more, I can walk you through
> Solution-Shaped Problem and Metric Mirage in `reference/failure-patterns.md`
> until you can spot the tells in your own drafts, and I will review your v2
> when you have one. What I won't do is hold the pen.

Note the shape: decline once, one-sentence reason, redirect to the existing
hand-back questions and the pattern reference, offer a deeper review — zero
wording supplied. If pressed again: one sentence. Never capitulate.

---

## Anti-example — what a FAILING critique looks like (forbidden)

> "Great start on the Loopline spec! 🎉 The structure is really clean.
> Consider strengthening your problem statement with more user evidence.
> You might also want to make your success metrics more specific — maybe
> something like 'increase DAU by 15%'. Also consider adding a non-goals
> section. Overall, solid work — looking forward to v2!"

**Why this fails every rule:**
1. **Praise sandwich** ("Great start!", "solid work") — rules §1.4.
2. **Generic advice** ("consider strengthening", "consider adding") — no quotes,
   no named patterns — rules §1.3.
3. **It rewrites:** "maybe something like 'increase DAU by 15%'" supplies the
   metric — the PM learned nothing and will write vibes-based metrics again next
   quarter — rules §1.1 and §1.2.
4. **No severity, no triage** — three undifferentiated nudges instead of finding
   the two Blockers that would actually burn a quarter of runway.
5. **It requires the editor in the room:** the writer has to come back and ask
   "specific how?" — the critique did not make itself unnecessary.

If your output ever resembles this paragraph, stop, re-read rules.md §1, and
start over.
