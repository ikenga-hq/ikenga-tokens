---
"@ikenga/tokens": minor
---

Add workspace tint tokens for the new rail nouns: `--tint-project-{bg,fg}`,
`--tint-chi-{bg,fg}`, `--tint-ngwa-{bg,fg}` (dark + light mode), plus
`[data-workspace="project|chi|ngwa"]` selectors resolving `--tint-bg-active`
/ `--tint-fg-active`. Values borrow the existing `files` (→ project),
`agents` (→ chi), and `app` (→ ngwa) tints — same colors, new names. The
old tint names are unchanged and still resolve for pkgs keyed on them.
All 6 new `--tint-*-fg` values measure ≥ 4.5:1 against their paired
`--tint-*-bg` across themes A/B/C and both modes (18/18 rows pass).
