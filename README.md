# Design Radar

A compact, evidence-filtered radar for current graphic and UI design change. Its job is to expose the few signals that can change a design decision now, not to archive every trend.

## Read order

On each run, read only:

1. `README.md`
2. `LATEST.md`
3. `index.json`

Do not recursively read `trends/`. Open a relevant trend file only when a candidate may duplicate, conflict with, weaken, strengthen, or change an indexed signal; maximum 3 trend files per run.

## Reader contract

For current-state questions, fetch the three files above by exact path from the repository default branch. Do not infer current state from code search hits, PR bodies, commit history, cached connector summaries, or how many `trends/*.md` files happen to be discoverable.

- `index.json` is authoritative for **which signals are currently active**. Count and enumerate every top-level entry when asked for the current radar.
- `LATEST.md` is authoritative for the compact current interpretation and prioritization of those active signals.
- `trends/*.md` contains supporting evidence and history; a trend file existing does not by itself mean the signal is active.
- If exact-path/default-branch reads are unavailable, say that the current radar cannot be verified. Do not answer from a stale search result or earlier PR snapshot.
- If `LATEST.md` and `index.json` disagree, treat `index.json` as authoritative for active membership and flag the inconsistency for maintenance.

## Research window

Prioritize work surfaced in the last 14 days and use roughly the previous 90 days as background for judging change. Start with Recent.design, Site of Sites, Brand New, Mobbin, Lapa Ninja, Design Spells, and Savee; follow through to original projects, studios, product pages, and first-party releases when needed.

Prefer real work, interfaces, pages, and screenshots. A headline, forecast article, individual opinion, or one high-profile project is not trend evidence by itself.

## Initialization baseline

The first populated radar run is broader than a normal incremental run. Survey the current ~90-day landscape across both graphic and UI design and establish the few active signals with the highest decision value. A signal does not need to be newly invented to enter the initial baseline: current recurrence may justify `stable`, while evidence across distinct recent batches may justify `growing`. Recent 14-day work should still be used to confirm that a baseline signal remains live.

After the baseline exists, return to incremental research and modify the repository only for substantive changes. Do not repeatedly rebuild the baseline.

## Promotion rules

- One project is evidence, not a trend.
- `emerging`: normally at least 3 independent projects across at least 2 independent sources.
- `growing`: the signal continues across distinct time batches.
- `stable`: the mechanism remains current and decision-relevant, but the recent window does not show meaningful acceleration or decline.
- `declining`: repeated current evidence shows the mechanism losing use or decision value; absence alone is insufficient.
- Separate what was observed from what is inferred.
- Record both `Fit` and `Avoid`.
- Do not turn a shared feature of good examples into a generation rule.
- Do not promote weak evidence into `LATEST.md`.

## Context budgets

- `LATEST.md`: at most 8 signals; target <= 900 tokens; roughly 60–100 tokens per signal.
- `index.json`: only `id`, `summary`, `status`, `fit`, `avoid`, `path`; target <= 1200 tokens total.
- `trends/<slug>.md`: detailed evidence; target <= 800 tokens each.
- Do not duplicate the same prose across files.

`LATEST.md` is working memory. Remove signals when they stop appearing, become ordinary practice, or lose decision value; historical trend files may remain.

## Updates

Only change the repository for a valid new signal, meaningful evidence change, status change, corrected definition, or removal from working memory. Otherwise make no repository change and create no PR.

For a substantive update, use `radar/YYYY-MM-DD`, change only relevant files, open a PR to `main`, and never auto-merge it. The PR should state Added, Changed, Removed, key evidence, main uncertainty, and whether the context budgets still pass.
