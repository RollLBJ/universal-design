# iOS and SwiftUI

- Follow Apple Human Interface Guidelines for the target OS. Prefer native navigation stacks, tab bars, sheets, alerts, menus and system text styles when appropriate. Use native back behavior, including edge gestures; do not duplicate system chrome.
- In SwiftUI prefer `NavigationStack`, `TabView`, `List` or lazy stacks, `.sheet`, and semantic fonts when supported by the deployment target. Integrate custom components without losing semantics. Use availability checks for newer APIs; do not raise minimum OS merely to adopt a style.
- Respect safe areas, status bar appearance, keyboard, home indicator and scroll content insets. Edge-to-edge backgrounds may extend beyond safe areas but interactive content should remain reachable. Use platform inset APIs rather than hardcoded device metrics.
- Default to at least 44 × 44 pt hit regions; account for Dynamic Type (including accessibility categories), VoiceOver, Reduce Motion and increased contrast. Use accessibility labels, values, traits, headings and meaningful reading order.
- Use SF Symbols when consistent with the app's icon language and license; provide appropriate accessibility names. Avoid imitation of system-only UI. Use system or existing licensed brand fonts.
- Verify compact phone and larger phone, large Dynamic Type, dark mode if supported, keyboard, sheet, back gesture and VoiceOver when tools are available.

Official guidance: https://developer.apple.com/design/human-interface-guidelines/ ; https://developer.apple.com/design/human-interface-guidelines/accessibility
