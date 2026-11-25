# Manual skill evaluation scenarios (not executed)

Run each task with the same model, starting repository, fixtures, tools, time budget and settings: A = no design skill, B = prior mobile skill or another relevant baseline, C = universal-design. Use fresh sessions and randomized anonymized outputs. Compare actual screenshots and behavior on the same runtime; record any inability to run. Repeat across seeds or sessions if possible. Do not treat model self-ratings as independent evidence.

| Task prompt | Observable acceptance checks |
|---|---|
| Redesign an existing Korean stock detail screen without changing its data layer. | Price, unit, timestamp and signed change visible; chart period and actual data; event sources; no fake insights; preserved navigation. |
| Build a SwiftUI note list and detail screen using existing project conventions. | Native back, list state, safe area, empty state, long text and Dynamic Type; working create/edit behavior if in scope. |
| Build an Android Compose search and filter flow. | Functional filters, no-results recovery, correct system back, keyboard/insets, 48 dp target default, font scaling. |
| Improve a Flutter transaction form without changing its submission API. | Persistent labels, validation, keyboard visibility, preserved inputs, duplicate submission protection, truthful result state. |
| Audit a React Native chat screen without changing code. | Evidence-based findings, composer and keyboard, scrolling, loading/error states, no modifications, limits reported. |
| Design a playful reading/discovery mobile app. | Distinctive brief-appropriate expression, real relevant imagery, not a forced minimalist dashboard. |
| Update a responsive marketing page. | Actual proposition, product evidence, responsive layout and keyboard focus; no forced mobile navigation. |
| Build a resizable desktop document workspace. | Document-centered layout, panels, keyboard navigation, preservation of selection and unsaved edits. |
| Review code using a text-only agent with no runtime. | Static findings only; no claimed screenshot inspection, runtime checks or invented scores. |

## Record

For each run record skill activation, files changed, build status, actual devices, screenshots, primary-path behavior, relevant hard gates, defects and reviewer preference. Use visual-review.md for the rubric. Have independent reviewers compare anonymous outputs where feasible, report counts and disagreements, and preserve untested criteria. No empirical improvement is claimed until these tests are run.

## Cross-model comparison

Repeat the same controlled A/B/C tasks across chosen model families, recording exact model versions, host tools and context budgets. Compare within each model before aggregating; report skill activation, task success, observed defect counts, reviewer agreement, test coverage, latency and token usage when available. Do not compare different tool access as though it were a skill-only effect.
