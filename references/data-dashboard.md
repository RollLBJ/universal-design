# Data-rich and financial screens

## First-screen hierarchy

Start with the user's primary question. Show a key value, unit, time range and relevant change, followed by the most useful trend or comparison. Add supporting factors, recent events and drill-down lower in the screen. Avoid equal-sized tiles for unrelated metrics. Dense screens may use a compact type role if readable at normal size and accessible scaling.

## Chart integrity

- Select line for time trends, bars for category comparisons, scatter for relationships, and tables for precise lookup. Bars should normally use a zero baseline. For line charts, disclose scale and meaningful truncation. Label units, time window and series; avoid misleading dual axes and 3D decoration.
- Use actual supplied values or explicitly labeled sample data. Indicate missing observations and stale data; don't silently interpolate or present cached values as live. Do not invent timestamps, sources, returns, confidence intervals or forecasts.
- Make tooltips accessible through tapping and an alternative to gesture interaction. Provide an accessible summary or data table for essential facts. Use labels, symbols, patterns or line styles in addition to color.
- Keep time range controls compact and legible. For event markers, show date, event title, source and distinguish observed correlation from demonstrated causation. Avoid marker overcrowding by clustering or filtering with disclosure.

## Finance specifics

Use locale-aware currency, signs, rounding and thousands separators. Show valuation date/time, currency and period; distinguish absolute change from percent change and realized from unrealized results. Use regional conventions for up/down colors when known (Korean equity interfaces often use red for rises and blue for falls); always include signs or labels. Do not infer performance from a color. Clearly separate reported facts, derived calculations and model-generated interpretation. For a transaction, review material details before submitting and display actual status. Avoid presenting fabricated insights as verified research.

## Example: stock research detail

1. Name/ticker, last available quote, signed change, timestamp.
2. Price chart, range selection, selected data point.
3. Event timeline with sourced dates and topic filters.
4. Theme drivers, evidence, counterevidence, uncertainty.
5. Reports and fundamentals in drill-down sections.

This is a pattern, not a mandatory template or financial recommendation.
