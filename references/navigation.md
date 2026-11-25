# Navigation and adaptive layouts

## Web and desktop

Use top navigation for a small set of public website destinations, sidebar or workspace navigation for persistent tools, and tabs for peer views within a context. Preserve URL/history behavior on web and document/selection context on desktop. Provide keyboard access, visible focus, and predictable modal dismissal. Adapt navigation to available width rather than forcing a mobile pattern.

## Mobile and touch

- Use bottom tabs or a platform-appropriate navigation bar for a small number of stable peer destinations (often 3–5). Do not turn creation or a modal action into a selected tab without a product reason. Show current destination through icon/text/state, not color alone. Preserve per-destination navigation and scroll state when appropriate.
- Push details onto a stack; back returns to the actual prior context. Use a sheet for short contextual tasks, a full screen for complex tasks, and an alert/dialog for a decision that genuinely requires attention. Do not open sheets inside sheets by default.
- Keep tab visibility predictable across the main flow; hide it only for intentionally immersive or focused tasks. Don't add redundant custom back controls or intercept system gestures without necessity.
- Deep links, notifications and restored sessions should resolve to a meaningful destination and a valid back stack. Handle missing objects and authentication requirements honestly.
- Respect safe areas, cutouts, system gesture zones, navigation bars, and keyboard insets. Use runtime insets rather than a device-specific magic number. Avoid applying the same inset twice.
- On tablets/foldables or expanded widths, consider sidebar/rail navigation, list-detail layouts, or a centered reading column. Preserve the same information architecture. Never just stretch buttons and paragraphs to fill width.
- Test back from nested details, sheet dismissal, switching tabs, restoring after rotation/background, and keyboard dismissal. Test landscape or explicitly document an intentional orientation constraint.
