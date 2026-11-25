# Android and Jetpack Compose

- Respect Material conventions and existing brand design. Prefer supported navigation, scaffold, top app bars, navigation bars/rails, bottom sheets and dialogs. Use the app's existing architecture; do not force Material 3 migration on a legacy project.
- In Compose use semantic `MaterialTheme` or established tokens, `Scaffold`, appropriate lazy layouts and stable state. Use Navigation Compose if already part of the project. Avoid hardcoding OS-specific appearance or assuming latest APIs exist.
- Support edge-to-edge with correct window insets for system bars, display cutouts and input method editor (IME). Account for gesture and three-button navigation; avoid double padding when combining scaffold and window insets. Respect system back and predictive back where supported.
- Aim for at least 48 × 48 dp touch regions. Use sp or scalable semantic text styles, TalkBack semantics, state descriptions and meaningful focus order. Decorative icons should not duplicate announcements. Honor system font scaling and display size.
- If dynamic color is used, check brand, status and contrast roles. Use existing light/dark schemes. Consider window size classes and foldables if supported. Keep gestures optional for essential actions.
- Test representative compact/expanded phones, font scaling, dark mode, keyboard, system back, and TalkBack where tools permit.

Official guidance: https://developer.android.com/design/ui/mobile ; https://developer.android.com/develop/ui/compose/accessibility ; https://support.google.com/accessibility/android/answer/7101858
