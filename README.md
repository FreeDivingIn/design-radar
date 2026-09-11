# Design Radar

A compact, evidence-filtered design memory for humans and AI. It tracks what is changing now, what has proven durable, and which historical languages are returning — without dumping the whole archive into model context.

## Three temporal lanes

- `LATEST.md` — **Now**. Recent design signals with current decision value.
- `EVERGREEN.md` — **Enduring**. Long-lived mechanisms that remain useful after novelty fades.
- `REVIVALS.md` — **Revival**. Historical design languages being reactivated in contemporary work.

The lanes are complementary, not a single trend lifecycle. A pattern becoming Evergreen is not the same as a trend declining. A Revival can simultaneously be growing.

## Minimum-context read order

Do not load all design knowledge by default.

1. Read `README.md` and `index.json`.
2. Route the task to the smallest useful lane set.
3. Read only the relevant compact lane entries.
4. Open at most 3 relevant `trends/*.md` files when evidence or deeper interpretation is needed.

Default retrieval for an ordinary design task should aim for:

- 1 relevant `current` signal
- 1 relevant `evergreen` signal
- optionally 1 relevant `revival`

Use only `LATEST` when the user explicitly wants what is new. Use Evergreen more heavily when the goal is durable, restrained, or low-risk design. Use Revivals when historical reference, cultural memory, nostalgia, or deliberate stylistic character is relevant.

## Index contract

`index.json` is the compact routing index and is authoritative for which signals are active across all lanes.

Each entry contains only retrieval fields such as `id`, `lane`, `summary`, `status`, `fit`, `avoid`, and `path`.

- `lane: current` maps to `LATEST.md`
- `lane: evergreen` maps to `EVERGREEN.md`
- `lane: revival` maps to `REVIVALS.md`

A file in `trends/` is evidence/history; its existence alone does not make it active.

## Current lane

`LATEST.md` answers: **What is changing now?**

- at most 8 signals
- primarily `emerging`, `growing`, or meaningful `declining` signals
- `stable` may remain temporarily when it is still current and decision-relevant
- a stable signal should eventually either lose current relevance, remain archived, or be evaluated for Evergreen promotion

One project is evidence, not a trend. `emerging` normally requires at least 3 independent projects across at least 2 sources. `growing` requires recurrence across distinct time batches.

## Evergreen lane

`EVERGREEN.md` answers: **What remains useful even when it is no longer fashionable?**

Do not promote a pattern merely because it has existed for a long time. It should show:

- **Longevity** — useful across a substantial time span
- **Transferability** — works across multiple products, brands, media, or contexts
- **Utility** — solves a stable design problem

Prefer durable relationships and mechanisms over recognizable surface features. Long-lived popularity alone is insufficient.

Target: at most 12 compact active Evergreen entries. The underlying evidence archive can be larger.

## Revival lane

`REVIVALS.md` answers: **Which historical design languages are becoming newly relevant, and what changed in their return?**

A revival requires:

- a verifiable historical anchor
- repeated current recurrence across independent projects

Record both `what returned` and `what changed`. Do not equate concept frequency with broad production adoption.

Target: at most 6 compact active Revival entries.

## Frontier vs adoption

Original concepts, experiments, student work, speculative design, Behance/Dribbble author projects, and experimental websites can be strong **frontier** evidence. Production products, commercial identities, Mobbin, Refero, and live product surfaces are stronger evidence of **adoption**.

Do not downgrade a concept simply because it is not shipped. Do not claim broad production adoption from concept work alone.

Trend and inspiration sites are discovery sources. Follow candidates to the original design object whenever possible: original project, author, studio case study, product, demo, prototype, or complete concept presentation. Analyze the original object rather than the aggregator's label, summary, crop, or montage.

## Research cadence

Weekly maintenance prioritizes work surfaced in the last 14 days and uses roughly the previous 90 days as context for current change.

Evergreen and Revival do not need a full rebuild every week. Re-evaluate them when new evidence suggests promotion, demotion, or revival, and perform a broader review roughly monthly.

## Context budgets

- `LATEST.md`: <= 8 signals; target <= 900 tokens
- `EVERGREEN.md`: <= 12 active entries; target <= 1200 tokens
- `REVIVALS.md`: <= 6 active entries; target <= 700 tokens
- `index.json`: compact routing metadata only; target <= 2000 tokens
- `trends/<slug>.md`: detailed evidence; target <= 800 tokens each

The database may grow indefinitely; default model context should not.

## Updates and merge policy

Only update the repository for substantive evidence, status, lane, definition, promotion/demotion, or active-set changes.

Use `radar/YYYY-MM-DD...` branches and PRs. A PR may auto-merge with squash only when changes are limited to Design Radar content, context budgets pass, evidence requirements pass, sources are accessible, and there is no material unresolved contradiction or risky repository/configuration change. Otherwise leave it for human review.
