# Design Radar

A compact, evidence-filtered radar for current graphic and UI design change. Its job is to expose the few signals that can change a design decision now, not to archive every trend.

## Read order

On each run, read only:

1. `README.md`
2. `LATEST.md`
3. `index.json`

Do not recursively read `trends/`. Open a relevant trend file only when a candidate may duplicate, conflict with, weaken, strengthen, or change an indexed signal; maximum 3 trend files per run.

## Research window

Prioritize work surfaced in the last 14 days and use roughly the previous 90 days as background for judging change. Start with Recent.design, Site of Sites, Brand New, Mobbin, Lapa Ninja, Design Spells, and Savee; follow through to original projects, studios, product pages, and first-party releases when needed.

Prefer real work, interfaces, pages, and screenshots. A headline, forecast article, individual opinion, or one high-profile project is not trend evidence by itself.

## Promotion rules

- One project is evidence, not a trend.
- `emerging`: normally at least 3 independent projects across at least 2 independent sources.
- `growing`: the signal continues across distinct time batches.
- Status is one of `emerging`, `growing`, `stable`, `declining`.
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
