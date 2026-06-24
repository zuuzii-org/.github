# .github — zuuzii organization profile

This repository powers the **organization profile** shown at
<https://github.com/zuuzii-org>.

## How it works

- GitHub renders **`profile/README.md`** from a **public** repo named **`.github`**
  at the top of the organization's Overview tab.
- The file must be on this repo's **default branch**.
- A `README.md` at the repo root (this file) is just the repo's own readme — it does
  **not** appear on the org page.

## Editing the profile

Edit [`profile/README.md`](profile/README.md). It uses only GitHub-allowed HTML
(`<div align>`, `<picture>`, `<table>`, `<img>`, `<sub>`, …) — no CSS/JS, which GitHub strips.

## Optional images

Images are optional; the profile looks complete without them. To add cover art,
team avatars, or a banner:

1. Drop the files into [`profile/assets/`](profile/assets/).
2. Uncomment the matching `<!-- cover → … -->` / `<!-- avatar → … -->` / `<!-- OPTIONAL banner … -->`
   block in `profile/README.md`.

Suggested sizes: banner ~1200×300, product covers ~600×360, avatars ~160×160 (square).
Relative paths like `./assets/foo.png` resolve to `profile/assets/foo.png`.
