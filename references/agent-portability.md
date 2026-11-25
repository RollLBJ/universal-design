# Model and agent portability

The skill is plain Markdown with standard Agent Skills metadata and relative references. No vendor API, model name, MCP server, plugin, image generator, specific command runner or API key is required. The host must support reading the skill or allow its text to be supplied manually. Instructions are not executable guarantees.

## Capability routing

| Available capability | Use | If unavailable |
|---|---|---|
| Read project files | inspect tokens, components and conventions | request relevant snippets only if necessary; mark assumptions |
| Edit files | implement within requested scope | provide concrete proposed changes, not a claim of edits |
| Run build/tests | use existing commands, check errors | mark runtime checks NOT TESTED |
| Browser/device/simulator | exercise task and capture screenshots | static review; no runtime claim |
| Image understanding | inspect actual captures, compare before/after | use objective checks from accessible layout/DOM/test output; mark visual inspection NOT TESTED |
| Asset generation/retrieval | use only when task warrants and rights/availability permit | reuse available assets or labeled placeholders; do not invent URLs |

Do not require an unavailable tool or attempt to bypass host permissions. If screenshots are captured but cannot be inspected, say so. A DOM audit is useful but is not a visual review. A browser is not a native simulator.

## Compact workflow for limited-context or smaller models

1. Read SKILL.md. Classify mode and platform. Read one relevant platform reference plus only the task-specific rules. For a new screen, load the core design and verification references in separate passes when context is limited.
2. Write a short contract (main task, anchor, hierarchy, visual character, tokens, states, checks) and keep it stable across files. For a narrow change inherit existing decisions.
3. Implement one screen or coherent flow at a time; reuse existing components. Keep the next small step explicit. Do not load every reference by default.
4. Run the highest-value available checks. Fix blocking issues first. Record what was actually observed, not what the model expects.
5. Return changed files or design proposal, test outcomes and remaining limitations. Never fill missing evidence with invented scores.

For larger multi-screen projects use a shared design token and component contract before parallel screen work. Avoid independent agents inventing separate palettes, typography or navigation. A supervising agent may merge and validate evidence; independent model opinions alone are not test results.

## Manual use without a skill loader

Supply SKILL.md as task context, followed by the relevant reference files. Ask the model to apply them to the existing project or provided screenshots. For text-only models request a design specification or code review rather than a visual-quality certification. Skill activation and instruction adherence depend on the host and model; evaluate rather than assume equivalence.
