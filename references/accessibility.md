# Accessibility and inclusive design

Use the platform's accessibility APIs and the applicable standards as design targets, not as a claim of legal compliance. WCAG means Web Content Accessibility Guidelines; use relevant contrast and interaction principles for native interfaces while following native platform requirements.

- Target normal text contrast of at least 4.5:1, large text 3:1 as defined by the applicable standard, and essential non-text control boundaries/state indicators 3:1 when applicable. Measure actual composited foreground/background colors, including overlays. Disabled/decorative exceptions are not a reason to make essential information faint.
- Recommended default touch regions: 44 × 44 pt on iOS and 48 × 48 dp on Android. Separate adjacent targets and ensure expanded hit regions do not overlap. For web, follow applicable WCAG target-size criteria and use larger targets for comfort.
- Support system text scaling and wrapping. Test long translations and larger accessibility categories. If fixed-height controls clip, redesign rather than suppress scaling. Don't use image-only text for essential content.
- Provide accessible names, roles, values, selected/disabled states and logical reading order. Decorative artwork should not add noise. Labels should match visible text. Announce meaningful errors and state changes. Use screen reader testing rather than assuming semantics are correct.
- Keep focus visible and usable for external keyboards and switch access where applicable. Do not require dragging, swiping, precise gestures, color, audio or vibration alone. Respect reduced motion and contrast preferences. Avoid flashing content.
- Validate core flows with VoiceOver/TalkBack where available. Automated scanners and contrast tools assist but do not replace manual testing. Mark checks as unverified if not performed.

References: https://www.w3.org/TR/WCAG22/ ; https://developer.apple.com/design/human-interface-guidelines/accessibility ; https://developer.android.com/guide/topics/ui/accessibility
