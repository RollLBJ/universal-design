---
name: universal-design
description: Design, build, redesign, or critique high-quality product interfaces for web, mobile, and desktop using any compatible agent or model. Use for UI design, UX improvements, visual systems, screen implementation, dashboards, native applications, websites, screenshot reviews, 화면 디자인, 앱 디자인, 웹 디자인, 디자인 개선, and UI 리뷰. Select platform-specific guidance only when relevant. Not for unrelated backend changes.
license: Apache-2.0
metadata:
  author: independent-community-adaptation
  version: "2.0.0"
---
# Universal Design

Create a coherent, distinctive product experience. Prioritize the user's task, legibility, functional correctness, accessibility and platform conventions. Visual originality must support the product; never force a fixed aesthetic. This skill is model-, vendor-, tool- and framework-agnostic.

## 1. Establish the design contract

Determine task mode (design proposal, implementation, redesign, review only), platform, audience, main task, product character and constraints. Inspect existing screens, tokens, component library, architecture and working flows when accessible. Preserve logic, data contracts and established product identity unless change is requested. Never modify code in review-only mode. Ask one focused question only when a material choice cannot be inferred; otherwise state assumptions.

Before implementation, record a compact contract: primary user task, dominant visual anchor, information hierarchy, navigation model, 3 observable visual attributes, color/type/density direction, reusable components, required states and acceptance checks. For small changes, inherit the existing contract and skip irrelevant work. Keep decisions specific to the product rather than copying a named app or inventing a new theme.

## 2. Load focused references

For new screens or redesigns read design-tokens, screen-patterns, visual-review and the relevant platform guide. For audits read visual-review and the references needed for the findings. For small changes use the smallest useful subset. If a file cannot be accessed, use the core rules below and report the limitation.

| Need | Reference |
|---|---|
| Composition, typography, tokens, component system | [design-tokens.md](references/design-tokens.md) |
| Screen-specific hierarchy and layouts | [screen-patterns.md](references/screen-patterns.md) |
| Navigation and adaptive layout | [navigation.md](references/navigation.md) |
| Feedback, motion, loading, errors, keyboard | [interaction-motion.md](references/interaction-motion.md) |
| Responsive websites, web apps, marketing pages | [platform-web.md](references/platform-web.md) |
| Desktop productivity apps, multi-pane workspaces | [platform-desktop.md](references/platform-desktop.md) |
| Native iOS / SwiftUI | [platform-ios.md](references/platform-ios.md) |
| Native Android / Jetpack Compose | [platform-android.md](references/platform-android.md) |
| Flutter, React Native, Expo, mobile web | [cross-platform.md](references/cross-platform.md) |
| Analytics, financial interfaces, charts | [data-dashboard.md](references/data-dashboard.md) |
| Accessibility and localization | [accessibility.md](references/accessibility.md) |
| Generic-looking, incoherent or overdecorated UI | [anti-patterns.md](references/anti-patterns.md) |
| Actual rendering, critique, tests and exit gates | [visual-review.md](references/visual-review.md) |
| Capability fallback and small-model workflow | [agent-portability.md](references/agent-portability.md) |

## 3. Compose a product-specific experience

- Choose one dominant content element and clear reading order for each decision context. Task-oriented screens start with the task; marketing and editorial pages may use an expressive hero when it conveys the actual value. Do not add a marketing hero to a utility, workspace or active conversation.
- Establish alignment, visual rhythm, intentional negative space and meaningful contrast. Use shared typography roles, semantic colors and consistent components. Use existing brand tokens first; adapt density and layout to the task and viewport. Avoid arbitrary one-off values and unearned visual effects.
- Differentiate screen archetypes: landing pages, lists, dashboards, workspaces, forms, readers, settings and discovery screens must not all be identical cards. Cards mark distinct objects or actions; group ordinary content through alignment, whitespace and dividers.
- Select imagery, illustration or custom visualization only when it adds meaning, using real available assets or clearly identified placeholders. Never invent asset URLs or display fabricated live data. A distinctive design can be restrained or expressive; avoid default gradients, icon tiles, badge clutter and repetitive panels unless justified.
- Use direct task-specific labels, accessible contrast, scalable text, meaningful state indicators and proper locale formatting. Support Hangul and other scripts with suitable font fallback. Never communicate essential meaning through color or motion alone.

## 4. Match the platform and implement the whole experience

- Web: semantic markup, responsive reflow, URL/history navigation, keyboard focus, actual links and controls, meaningful loading and error states. Do not force mobile tab bars onto desktop websites.
- Mobile: native navigation and back behavior, safe areas, keyboard insets, touch regions (iOS 44 pt / Android 48 dp recommended defaults), gestures with accessible alternatives, optional haptics and scalable text. Do not simulate operating-system chrome inside an app.
- Desktop: resizable windows, appropriate menus/toolbars/sidebars, keyboard shortcuts, focus, pointer and selection behavior, adaptive panes. Do not stretch a phone layout or force a marketing layout onto a workspace.
- Choose one primary action per decision context and preserve useful secondary actions. Implement normal, loading, empty, error, offline/stale, permission, input validation, pending, success and disabled states as relevant. Preserve user input and prevent duplicate submissions. Show confirmation only after actual success.
- Reuse the project's framework and components. Use real state, navigation and data contracts. Every visible control must work or be explicitly labeled as unavailable in a prototype. Do not introduce unrequested dependencies, external services or fake functionality for visual appeal.
- Handle long labels, narrow and wide viewports, keyboard navigation, text scaling, dark mode where supported and reduced motion. Optimize asset sizes and repeated content. Avoid claims about performance without measurement.

## 5. Render, critique, fix and verify

Use available project tools; do not presume access to a browser, simulator, shell, image generator or vision model. Follow [agent-portability.md](references/agent-portability.md) for capability fallbacks. In implementation mode, run the project's existing checks, capture real screenshots where possible, inspect them if vision is available, exercise the primary task and relevant edge states, then fix high-impact issues and retest. Check the relevant platform sizes, keyboard/focus, accessibility and scrolling. For redesigns compare before/after when available. A mockup, a successful build or a generated image is not evidence of functioning UI.

Use [visual-review.md](references/visual-review.md) for hard gates and diagnostic scoring. Default to two focused passes when tools permit. Do not claim an observed score for untested categories; a high score never overrides broken functionality, misleading data or inaccessible essential controls. In review-only mode report findings without editing. In design-only mode provide a design contract and implementation/test plan, not a claim of implementation.

## 6. Delivery

Provide the selected direction, changed screens/files (if any), essential behavior, actual test evidence and remaining issues. Distinguish observed, inferred and untested findings. Do not claim screenshot inspection without vision, runtime testing without execution, or production readiness without appropriate validation. Respond in the user's language. Keep the original scope and avoid unnecessary features.
