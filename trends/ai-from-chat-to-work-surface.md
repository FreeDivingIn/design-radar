# AI moves from chat sidecar into the work surface

Status: `growing`

## Observation

Across recent product releases, generated UI is increasingly placed inside the user’s existing work context and remains directly manipulable after generation.

- **Figma** put its design agent directly on the canvas, then added properties and in-context annotations to Figma Make so users can point, manipulate and prompt the same artifact.
- **Google Sheets Canvas** turns source rows and columns into prompt-generated, read-write dashboards, Kanban boards and other mini-apps layered directly on spreadsheet data.
- **SAP Joule Work** uses a compositional design system to generate “Spaces” around user intent and context rather than requiring navigation through a fixed generic dashboard.

## Inference

AI UI is moving beyond a conversational side panel toward a reversible work surface: generation proposes a structure, while direct manipulation, source data and familiar controls remain available. The important design variable is the relationship between generated view and durable underlying artifact.

## Fit

Creation, analysis and operational workflows where users need to explore multiple representations or assemble task-specific tools from existing data/content.

## Avoid

High-stakes or tightly regulated flows where generated structure makes permissions, auditability, state location or recovery harder to verify; simple deterministic tasks better served by fixed UI.

## Evidence

- [Figma design agent](https://www.figma.com/blog/the-figma-agent-is-here/) — May 2026 launch puts the agent directly on the design canvas.
- [Figma Make properties and annotations](https://www.figma.com/blog/properties-panel-and-annotations-now-in-figma-make/) — July 2026 adds direct visual editing and pointed prompting.
- [Google Sheets Canvas](https://workspaceupdates.googleblog.com/2026/08/use-google-sheets-canvas-to-visualize-data.html) — August 2026 introduces generated read-write interfaces over spreadsheet data.
- [SAP compositional design system](https://www.sap.com/central-asia-caucasus/design/stories-resources/evolving-design-systems-for-ai-driven-ux) — Joule Work composes workspaces around goals, roles and context.

## Uncertainty

The pattern is strongest in AI-native or AI-expanded products and still carries major predictability and governance questions. `growing` reflects independent releases across several recent time batches, not universal suitability.
