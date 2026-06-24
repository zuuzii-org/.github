# .github — zuuzii organization profile

This repository powers the **organization profile** shown at
<https://github.com/zuuzii-org>.

## How it works

- GitHub renders **`profile/README.md`** from a **public** repo named **`.github`**
  at the top of the organization's Overview tab.
- The file must be on this repo's **default branch**.
- A `README.md` at the repo root (this file) is just the repo's own readme — it does
  **not** appear on the org page.

## Layout

```
profile/
├── README.md              ← org landing (English, default)
├── README.zh.md           ← org landing (中文)
├── products/
│   ├── <slug>.md          ← product detail page (English)
│   └── <slug>.zh.md       ← product detail page (中文)
└── assets/
    ├── banner-{light,dark}.svg        ← English banner
    ├── banner-zh-{light,dark}.svg     ← 中文 banner
    └── products/<slug>/…              ← per-product images
```

slugs: `aihunter` · `museview` · `agentstudio` · `token-share` · `ai-warmup` · `chatbot`

## Languages

English is the default landing page; each page has an `English · 中文` toggle at the top.
Links rendered on the **org page** (the main README) must be **absolute** blob URLs —
relative links resolve against the org root there and 404. Links inside the product pages
(viewed as normal files) may be relative.

## Editing

Edit the matching language file. HTML stays inside GitHub's allowlist
(`<div align>`, `<picture>`, `<table>`, `<img>`, `<sub>`, `<details>`) — no CSS/JS, which GitHub strips.
Banners are SVG (style is baked into the image). Product images live under `profile/assets/products/<slug>/`.
