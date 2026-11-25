# Flutter, React Native, Expo and mobile web

## Flutter

Use existing `ThemeData`, `ColorScheme`, text styles and widget architecture. Apply `SafeArea` selectively; handle keyboard via `MediaQuery` and appropriate scaffold behavior. Use `LayoutBuilder` or available constraints for adaptive layout rather than assuming device model. Preserve semantics, focus and text scaling; verify Cupertino/Material navigation matches the target and app direction. Avoid unnecessary dependencies and fixed heights for text.

## React Native / Expo

Reuse existing theme and routing (e.g. Expo Router or React Navigation if already installed). Prefer platform-aware safe area handling, accessible `Pressable` controls, appropriate keyboard avoidance and virtualized lists. Respect system font scaling, screen reader semantics, back behavior and native navigation. Do not replace native controls with WebView merely for appearance. Check installed library versions before proposing APIs.

## Mobile web / progressive web apps

Use semantic HTML, correct viewport configuration, flexible layout and real buttons/inputs. Handle safe-area env insets if applicable, dynamic viewport sizing, on-screen keyboard, zoom, pointer and keyboard focus. Use touch-friendly sizes (44 CSS px as a comfortable default, not a native equivalence). Do not disable user zoom. Avoid hover-only interactions. Implement history navigation and deep links. Test actual mobile browsers when possible; responsive desktop screenshots cannot establish native app behavior.

## Shared

Keep common brand identity but allow native differences in back, menus, sheets, permission dialogs, haptics and accessibility. Respect installed SDK versions; run the existing build scripts rather than inventing an environment. Use the project's dependency policy. Do not claim cross-platform verification from a single runtime.
