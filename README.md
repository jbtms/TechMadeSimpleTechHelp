# Tech Made Simple — Tech Help Landing Page

Landing page for **Tech Made Simple** (tech help for seniors and non-technical people), part of [TechMadeSimple.online](https://techmdesimple.online).

**Live URL:** `techhelp.techmdesimple.online`
**AI Consulting branch:** `techmdesimple.online/ai-consulting`

---

## Before Going Live

Search `YOUR_CAL_LINK_HERE` in `index.html` — there are ~10 instances. Replace every one with your Cal.com event link (e.g. `jaron-banks/intro`).

Once replaced, also uncomment the Cal.com inline embed block near the bottom of `index.html` (inside the `<script>` tag labeled "Cal.com: initialize inline embed").

---

## Local Preview

```bash
python3 -m http.server 3000
# then open http://localhost:3000
```

Or if you have Node:
```bash
npx serve .
```

---

## GitHub Pages Deployment

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set Source: `main` branch, `/ (root)` directory
4. Set Custom domain: `techhelp.techmdesimple.online`
5. In your DNS (Cloudflare or registrar), add:
   ```
   CNAME  techhelp  →  your-github-username.github.io
   ```
6. GitHub will auto-provision an SSL certificate via Let's Encrypt

**Optional redirect:** In Cloudflare, add a redirect rule:
`techmdesimple.online/tech-help*` → `https://techhelp.techmdesimple.online` (301)

---

## Brand Tokens

| Token | Value | Usage |
|---|---|---|
| `--brand-blue` | `#1A56DB` | Primary color, nav, icons |
| `--brand-red` | `#E3231A` | CTA buttons, accents |
| `--ink` | `#0D0D0D` | Headlines |
| `--ink-muted` | `#4A4A5A` | Body text |
| `--surface` | `#F7F8FC` | Section backgrounds |
| `--blue-light` | `#EBF1FD` | Icon badges, tint backgrounds |

Fonts: **Fraunces** (headings) + **Inter** (body)

---

## File Structure

```
TechMadeSimpleTechHelp/
├── index.html          ← Full landing page (all styles inline)
├── CNAME               ← GitHub Pages custom domain
├── README.md           ← This file
└── brand_assets/
    ├── TechMadeSimpleLogo.png
    └── fgBvOghPTVnVjizDVmjC.png
```
