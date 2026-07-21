# Spec Editor — an AI editor for early-stage product specs

An editor for **product specs written by early-stage PMs** (pre-seed → Series A,
typically one of the first 1–3 PM hires), reviewing specs **before engineering
handoff**.

It does not rewrite your spec. It reads like a senior product lead, quotes your
exact words back at you, names the failure pattern, explains why it matters at
*your* stage — and hands the problem back to you to fix. A spec the editor fixes
teaches you nothing. A spec you fix yourself is the skill.

## Who this is for

- **First PMs and founder-PMs** with no senior product person reviewing their
  work before it hits engineering
- **Career-switching PMs** (from eng, design, ops) who are strong on execution
  but uncalibrated on spec craft
- **Small eng teams** tired of mid-sprint scope fights that a sharper spec would
  have prevented

## Quick start (60 seconds)

1. Drop this folder into a Claude project (or any AI tool that accepts file
   context). **Include the whole folder** — the `reference/` files are
   load-bearing: the editor names failure patterns from them and calibrates
   severity by stage. `rules.md` alone will not work.
2. Paste your spec. Optionally add one line of company context
   ("12 people, 5 engineers, seed") — if you don't, the editor assumes
   pre-seed and says so.
3. Get back a critique: stage line, verdict, 3–5 severity-ranked findings, and
   "the one thing" — the single highest-leverage fix, as *your* task.
4. Revise, then bring back your v2 — the editor reviews revisions with the same
   rigor. That loop is where the calibration compounds.

## What a finding looks like

> **[🔴 Blocker] — Solution-Shaped Problem**
> **Quote:** "Our users can't get AI-powered summaries of their Slack channels…"
> **What's wrong:** The problem statement names your product and your feature…
> **Why it matters at this stage:** At pre-seed you are not optimizing a product,
> you are searching for one…
> **Hand-back question:** What did you observe a specific user doing — in their
> actual workflow, without your product — that cost them something?

No rewritten sentences. No "consider strengthening." No praise sandwiches.
Every finding cites your words, names the pattern, and ends with a question only
you can answer — in the document.

## What it will NOT do

- ❌ Rewrite your spec, a section, or a single sentence (even if you ask)
- ❌ Suggest wording, sample metrics, or example problem statements
- ❌ Grade roadmaps, vision decks, or go-to-market plans (specs only)
- ❌ Copy-edit typos
- ❌ Give you 14 comments — it gives you the 3–5 that matter, ranked

If you ask it to "just rewrite it," it will refuse once, tell you why, and offer
to deepen the critique instead. That refusal is the product.

## File map

| File | Its one job |
|---|---|
| `identity.md` | Who the editor is and what work it reviews |
| `rules.md` | How it critiques: prime directive, forbidden behaviors, protocol, severity, output format |
| `examples.md` | What good critique looks like — 3 worked examples (pre-seed, seed, Series A) + refusal exhibit + 1 forbidden anti-example |
| `reference/spec-anatomy-checklist.md` | The load-bearing sections of a spec and how they go hollow |
| `reference/failure-patterns.md` | 13 named failure patterns with tells and mechanisms |
| `reference/stage-calibration.md` | How rigor changes pre-seed → seed → Series A |

## Why "editor, not rewriter"?

Reviewing work is one of the highest-leverage skills in any company — senior
people are paid to catch the mistakes junior people make. This editor encodes
that judgment as reusable context: 13 named failure patterns
(Solution-Shaped Problem, Vibes-Based Evidence, Ghost Non-Goals, Metric
Mirage, Automation Without a Floor…), a severity model calibrated to company stage, and a hard behavioral
contract against drifting into ghostwriting.

The bar: someone with no context hands it a spec and gets back feedback that
actually improves it — because the *writer* does the improving.

## License

MIT. Use it, fork it, calibrate it to your own team's failure patterns.
