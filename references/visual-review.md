# Screenshot-driven visual review and exit criteria

## Evidence workflow

1. Identify the target screen, platform/runtime, device sizes, theme, data and acceptance path. Capture baseline for redesign if available.
2. Build/run using the project's commands. Capture actual viewport and key scroll positions using the available emulator/simulator/device/browser. Do not generate a mock image and call it a screenshot. Inspect the screenshots if image understanding is available, not just their filenames. If not, mark visual inspection NOT TESTED even if screenshots were captured.
3. Test primary path plus relevant loading, empty, error, offline, long content, keyboard, back and selection states. For an existing app compare baseline and final. Test compact and expanded widths for the target platform, resizable desktop windows, keyboard/focus, text scaling and light/dark if applicable. Use a deterministic fixture for difficult-to-reproduce states, marked as a fixture.
4. Record issues with screen/state, severity, evidence, fix and retest. Prioritize blocking functionality, accessibility and layout defects over cosmetics. Fix within scope, recapture, and repeat. Default to two focused passes if feasible; do not mask unresolved defects to meet an arbitrary iteration limit.
5. Report exact checks and limitations. Record each as PASS (observed), FAIL, NOT TESTED or N/A with reason. Build passing is not visual verification. A screenshot is not proof of a working interaction. A web preview is not native verification.

## Hard gates (fail or unverified cannot be reported as fully validated)

- Main task works without a dead end, incorrect result, or misleading status.
- Essential text and actions are visible, usable, not clipped or covered by system bars/keyboard.
- Back/navigation works and no required action is gesture-only or inaccessible by design.
- Key accessibility checks (target sizes, contrast, text scaling and semantics) meet chosen requirements, or gaps are explicitly recorded.
- No regressions in critical existing flows observed in the tested scope. No fake data presented as actual results.

## Optional diagnostic scoring

Rate each category 0–4 using evidence: 0 = unusable, 1 = major issues, 2 = usable with significant issues, 3 = solid with minor issues, 4 = strong in observed scope. Use N/T for untested, N/A only when irrelevant. Score = sum(weight × rating/4) for assessed categories, with coverage = sum(assessed weights)/sum(applicable weights). Report observed subtotal and coverage; do not report a full score if any applicable category is untested. An indicative 85/100 goal is a heuristic, not a validated metric or replacement for hard gates.

| Category | Weight |
|---|---:|
| Hierarchy and legibility | 20 |
| Functional usability | 20 |
| Platform fit | 15 |
| Visual consistency | 15 |
| Product-specific expression | 10 |
| States and feedback | 10 |
| Accessibility | 10 |

If all applicable categories are assessed, normalize score by applicable weights. An untested gate is unresolved, not an automatic pass. For review-only tasks, provide evidence-based findings and recommended fixes; do not implement without permission.

## Evidence record template

| Screen / state | Runtime / size | Check | Result | Evidence / issue | Retest |
|---|---|---|---|---|---|
| [screen] | [actual] | [test] | PASS/FAIL/NOT TESTED/N/A | [actual path or observation] | [result] |

Deliver a short summary of design direction, changes, tested environments, evidence and open risks. If the only available artifact is source code, clearly distinguish static inspection from execution. Never claim visual quality, accessibility compliance or production readiness solely from a score.
