# CTA weight scales with task orientation

Status: `stable` (Evergreen)

## Observation

In the same dataset, 81.8% of annotated sites present the primary call to action as a button — but the share scales systematically with task orientation: web apps 97.2%, desktop apps 96.1%, design tools 95.6%, productivity 94.6%, finance 91.8%, versus portfolio 56.6% and agency 64.2%. The pattern is stable across batches (77.3% → 82.2%, ns; direction slightly up). Where buttons recede, text links take over (327/2,208 sites) — concentrated in expressive contexts.

## Mechanism

An explicit button is an unambiguous action affordance, and its appropriate visual weight tracks the visitor's intent frequency. Task-oriented visitors arrive ready to act, so maximum affordance costs nothing and converts; expressive-context visitors arrive to browse, where a heavy button reads as pushy and a text link preserves tone. The durable relationship is not "use buttons" but grading action weight to intent.

## Fit

Signup, purchase, trial and download flows; any page whose visitor arrives with a task already formed.

## Avoid

Applying maximum-strength CTA styling in editorial or portfolio contexts where it reads as pushy; or hiding the primary action entirely in task flows, where an unstyled link under-serves ready intent.

## Evidence

- Dataset measurement as above (primary CTA annotation: button 1,719 / text-link 327 / none 160 of 2,208).

## Uncertainty

CTA annotation comes from a local 7B vision model (not remote-adjudicated like hero type); category-level gradients are nonetheless large relative to annotation noise. Same cross-sectional longevity caveat as other dataset-backed entries.
