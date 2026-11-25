# Desktop applications and professional workspaces

Applies to macOS, Windows, Linux, Electron, Tauri and other desktop interfaces. Preserve established framework and OS conventions. Design for precision, keyboard and pointer efficiency, resizable windows and repeated professional use.

- Choose the appropriate structure: document-centered, sidebar + detail, multi-pane workspace, inspector, table or canvas. Give the main work surface the dominant area. Reserve permanent navigation/inspector panels for frequent tasks; collapse or resize where useful. Avoid mobile-sized cards and gratuitous marketing copy.
- Define minimum usable window dimensions based on content. Adapt panels when windows narrow, preserve important context, constrain long reading text and avoid blanket horizontal overflow. Allow scroll for genuinely wide data tables/canvases; keep row/column context where needed.
- Support expected keyboard shortcuts, focus order, menus, context menus, undo/redo and selection behavior where relevant. Do not override OS or browser shortcuts unnecessarily. Never make context menus or hover the only way to perform an essential action.
- Preserve document state, selection and unsaved edits on navigation; use clear dirty/saving/saved/error states. Confirm destructive actions proportionally. Respect system window chrome, theme, contrast and text scaling. Do not imitate privileged OS dialogs.
- Use dense rows when they improve scanning, but keep controls readable. Align comparable values; use sortable tables for precise lookup and charts for trends. Provide meaningful empty, loading, offline and permission states.
- Verify narrow and wide windows, keyboard-only navigation, panel resizing, scroll behavior, selected states, long data, dark mode where supported and primary workflow. Test native packaging/runtime separately from a browser preview when applicable.
