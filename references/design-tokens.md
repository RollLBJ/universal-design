# Design system and composition

## Start with a product-specific direction

Choose three observable attributes (e.g. calm, compact, high-contrast), then translate them into type weight, density, surfaces and accent usage. A finance app may emphasize precise numerals and a clear chart; a book app can emphasize editorial typography; a creative app may use expressive color and imagery. Do not treat any style as universally correct.

Use existing tokens first. For a new project the following are starting values, not device-independent requirements. In native iOS use logical points; Android uses dp for geometry and sp for scalable text; Flutter/React Native use logical units and platform-aware text scaling. For web use CSS pixels or relative units; for desktop use the framework’s logical units and system scaling. Do not equate these with physical pixels. The table below is a comfortable mobile-oriented starting point; desktop workspaces may use denser rows and web typography may vary by content.

| Role | Default starting value |
|---|---|
| spacing | 4, 8, 12, 16, 24, 32, 40 |
| horizontal page inset | 16–24, adaptive at larger widths |
| section separation | 24–32 |
| row height | content-driven; typically 48–64 |
| title | 28–32, semibold/bold |
| section heading | 20–24, semibold |
| body / control label | 15–17, normal/medium |
| secondary label | 13–14, scalable and contrast-safe |
| chart metadata | 12–14 if legible; never the sole source of essential facts |
| primary control | 48–56 logical units high, grow for text |
| small/medium/large corner radii | 8 / 12 / 20, adjust to visual direction |
| hit area | iOS 44 pt, Android 48 dp recommended defaults |

Use semantic typography roles instead of independently selecting sizes on each screen. Let platform type scales and user accessibility settings override base sizes. Avoid forced uppercase, excessive letter spacing (especially for Hangul), and arbitrary truncation. Korean body line height often benefits from 1.45–1.6 as a starting point; verify with actual glyphs. Use font fallback covering the app's languages. Number alignment must not require a separate font.

## Color and surfaces

Define background, surface, raised surface, text primary/secondary, separator, accent/on-accent, selected, disabled and semantic states. Begin with one accent, add others only for clear categories or meaning. Use tinted surfaces, elevation, or dividers selectively. Dark mode requires independent contrast checks; do not just invert colors. Validate normal text at 4.5:1 and large text at 3:1 as applicable; non-text essential boundaries at 3:1 against adjacent colors where required. Do not assume a sample palette meets these ratios without measurement.

## Composition and density

Use a shared alignment axis for text and controls; break it deliberately for full-bleed media. Set a single dominant visual anchor. Avoid repeated equal-weight tiles unless items really are equal. Prefer aligned rows with optional dividers for repeated records. Reserve containers for items with independent meaning. Use responsive width constraints for reading, and split views only when enough space exists. Keep the final item above persistent controls and system insets. Do not hardcode screen heights.

## Component contract

Define anatomy, variants, interactive states, content bounds, accessible labels and token use for buttons, fields, list rows, tabs, chips, sheets and cards. Reuse the same control for the same behavior. Use a chip when it is a filter, selection, or meaningful status, not merely a label background. Prefer text for low-priority metadata. Buttons use verbs and state their result; icons use a consistent family and optical size. An icon's visual bounds can be smaller than its hit region.
