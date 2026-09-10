# Motion sparsifies into accents

Status: `emerging`

## Observation

Same dataset and batches as the photography signal. Median static ratio (share of scroll-preview frames with no visible change) rose 0.138 → 0.199 (+43.6% relative; 1,227 → 265 videos), and mean motion intensity fell 15.4% relative. The rise persists within the Animated-tagged stratum (0.128 → 0.183), so it is not explained by tag mix. All newly added sites ship scroll previews, versus 63% in the baseline batch.

## Inference

Two readings remain open. (a) Motion design is shifting from ambient, continuous animation to sparse accents at section transitions. (b) Baseline previews were recorded selectively for motion-rich sites, inflating baseline motion. Persistence within the Animated stratum leans toward (a), but recording selection cannot be excluded from a single source.

## Fit

Motion-budget decisions: motion as punctuation at transitions rather than permanent ambience.

## Avoid

Acting on this signal before independent corroboration — the selection confound is unresolved. Cross-site motion comparison needs static-ratio correction; raw intensity mixes in scroll displacement.

## Evidence

- [santos.fyi](https://santos.fyi/) — static ratio 0.65.
- [Displace](https://displace.agency/) — static ratio 0.60.
- [Unmoth](https://unmoth.com/) — static ratio 0.60.
- Frame-level measurement over 1,492 decoded scroll previews (2 fps sampling).

## Uncertainty

Weakest of the three candidates from this batch: unresolved recording-selection confound on top of the single source. Held out of `index.json` and `LATEST.md` pending independent verification.
