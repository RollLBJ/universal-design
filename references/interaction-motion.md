# Interaction, state and motion

| State | Required behavior |
|---|---|
| Initial loading | stable layout or appropriate indicator; no misleading values |
| Refresh | keep valid previous content where possible; show refresh status |
| Empty | say what is absent, why if known, and relevant next action |
| No search matches | preserve query and offer filter reset/change |
| Recoverable error | specific message, retry, preserve inputs |
| Offline / stale | distinguish cached from live data, show freshness, allow safe actions |
| Permission denied | explain feature impact, offer settings or alternative, don't loop prompts |
| Pending submission | avoid duplicates, keep progress and cancellation if safe |
| Success | only after confirmation, make result and next action apparent |
| Disabled | reason where not obvious; distinguish from loading |

Skeletons suit predictable layouts, not every request; progress indicators suit operations with unknown structure. Avoid layout shifts when content resolves. For long-running work distinguish determinate progress from indeterminate progress. Announce meaningful errors and results to assistive technologies without flooding announcements.

## Pointer, touch and keyboard

For web/desktop provide appropriate hover, focus-visible, active, selected and disabled states; hover is enhancement, not the only way to discover essential actions. Support standard keyboard activation, shortcuts when relevant and visible focus.

Provide pressed and selected states, a labeled alternative to gesture-only actions, and appropriate undo or confirmation for destructive operations. Reserve haptics for important feedback, respect user settings, and never make vibration the only signal. Prefer platform-standard scroll and gestures; nested scroll must have a reason. The keyboard must not cover active fields or essential actions; use runtime insets, focus management and scrolling. Test multiline fields and physical keyboards where relevant.

## Motion

Use platform navigation transitions. For custom feedback start around 120–200 ms; for small component transitions 180–300 ms, adjusting to platform feel and distance. Avoid mandatory waits and perpetual decoration. Animate properties efficiently, avoid heavy blur/large raster work in scrolling lists. Honor reduced motion, replacing nonessential movement with simple changes. Measure on a real or representative runtime before claiming smoothness.

## Performance

Use appropriate lazy lists, stable keys, thumbnail sizing and cancellation. Avoid unnecessary fetches and recompositions on scroll; preserve state when navigating. Test slow-network and rapid-tap scenarios where practical. Do not invent frame-rate or latency measurements.
