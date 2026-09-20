---
"@ikenga/tokens": patch
---

Workspace tints now actually apply. The `[data-workspace="…"]` rules that resolve `--tint-bg-active` / `--tint-fg-active` were bare attribute selectors (0,1,0), while the defaults they were meant to override are declared inside `:root[data-mode='dark']` and `:root[data-mode='light']` (0,2,0) — so they lost on specificity regardless of source order, and every workspace painted the mode default blue. All eleven rules are now `:root[data-workspace="…"]`, matching what the mode rules already do.

This affects the three rail nouns added in 0.5.0 (`project`, `chi`, `ngwa`) and the eight older tints (`app`, `mail`, `outbox`, `studio`, `agents`, `files`, `sessions`, `settings`) alike — none of them had taken effect.
