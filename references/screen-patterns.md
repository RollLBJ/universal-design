# Screen patterns

Choose by user task, not by a default template. These are structural suggestions, not mandatory layouts.

| Screen | Opening viewport | Below / next action | Avoid |
|---|---|---|---|
| Home | main status, relevant recent item or resume action | prioritized shortcuts, activity | generic welcome banner |
| Dashboard | primary metric with period and comparison | supporting metrics, drill-down | uniform metric tiles without context |
| List / feed | title, useful search/filter, first real items | pagination, details | nested card per text row |
| Detail | object identity, key fact, most useful action | sections, provenance, related items | repeating summary and title |
| Search | focused query and recent/suggested results | filters, results, no-match recovery | unrelated promotional material |
| Form | task title and first field | logical groups, submit, validation | placeholder-only labels |
| Settings | grouped settings and current values | deeper settings, account actions | decorative dashboard layout |
| Onboarding | clear value or immediate task | progressive setup, skip where possible | mandatory multi-slide marketing |
| Reader | document title or resume point, readable content | bookmarks, search, navigation | persistent controls hiding content |
| Chat | current conversation, clear composer | streaming, stop/retry, attachments | unnecessary welcome in an active thread |
| Media / discovery | actual visual content | contextual filters and details | filler imagery unrelated to subject |
| Transaction | amount, recipient, meaningful confirmation | review, result, recovery | ambiguous primary action |

## Lists and details

Keep primary and secondary text aligned and predictable. Make the row tap target match the action; disambiguate overflow actions. Show loading and partial failure at the appropriate scope. Preserve filters, selected item and scroll position when returning. Do not hide all labels behind horizontal scrolling. For drill-down, use a stable title and real back behavior.

## Forms and transactions

Use persistent labels, appropriate input types and keyboards, validation near the field, and a readable review before high-impact submission. Avoid showing errors before the user can act. Preserve input after a recoverable error. Disable duplicate submissions, communicate pending status, and distinguish failure from unknown outcome. Never show a success screen without confirmation from the relevant state.

## Chat and content

Keep composer visible above the keyboard; grow it up to a sensible limit. Preserve draft and scroll anchor; autoscroll only if the user is following the tail. Provide a return-to-latest affordance when reading history. Make retry, cancellation and partial output states explicit. For reading, prioritize text size, line spacing, selection and navigation; don't compete with content using animated chrome.

## Korean/localized apps

Prefer short natural Korean action labels (저장, 다시 시도, 종목 추가). Do not add English labels solely for aesthetics. Use locale-aware date, currency, decimal and units; handle names and long strings without clipping. Test actual translations, not just ASCII fixtures.

## Additional platform archetypes

- Landing: specific proposition, actual product evidence, useful next action; then supporting proof and details.
- Desktop workspace: document, canvas or table with essential tools; contextual inspector and actions.
- Commerce: actual product, availability, price, specifications, delivery and clear purchase flow; no hidden costs or artificial urgency.
