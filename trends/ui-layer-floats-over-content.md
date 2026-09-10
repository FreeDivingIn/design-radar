# Functional UI becomes a floating layer over content

Status: `stable`

## Observation

Apple-platform interfaces continue to separate content from navigation/actions as two visual layers: content extends edge-to-edge while native controls float above it, shrink or morph with context, and recede when attention should stay on reading, creating or watching.

- **Apple’s 2026 guidance** explicitly defines a floating UI layer for tab bars and toolbars above a content layer, with brand expression pushed primarily into content.
- **Slack** extends conversations to screen edges, uses floating glass headers/search/composer controls, and relies more heavily on native components.
- **Tide Guide** combines full-screen weather visualization with Liquid Glass controls and adaptive color tied to the sky.
- The mechanism continues from the iOS 26 introduction into 2026 platform refinement, so it is current but no longer appropriately classified as emerging.

## Inference

On Apple platforms, persistent solid app chrome is giving way to a platform-owned functional layer that preserves access while visually yielding to content. The decision is about layer ownership and adaptive control behavior, not about copying a glass material.

## Fit

Native Apple apps centered on media, reading, creation, communication or spatially rich content, especially when standard navigation/actions can use platform components.

## Avoid

Dense web/data products, custom controls whose meaning depends on persistent boundaries, or surfaces where transparency/motion harms contrast and accessibility.

## Evidence

- [Apple WWDC26: Communicate your brand identity on iOS](https://developer.apple.com/videos/play/wwdc2026/251/) — defines separate floating UI and content layers.
- [Apple app integration showcase](https://developer.apple.com/videos/play/meet-with-apple/208/) — documents the content-first goal and multiple third-party implementations.
- [Slack iOS 26 redesign](https://slack.com/blog/news/redesigning-slack-ios26) — first-party account of edge-to-edge content and floating controls.
- [Tide Guide](https://tideguide.com/) — current product describes full-screen charts, adaptive palette and Liquid Glass integration.

## Uncertainty

This is strongly platform-specific. `stable` means it is an established current Apple design direction with ongoing adoption/refinement; it should not be projected onto web or cross-platform UI by default.
