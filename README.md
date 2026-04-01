# Tech Made Simple — Tech Help Landing Page

Landing page for **Tech Made Simple** (tech help for seniors and non-technical people), part of [TechMadeSimple.online](https://techmdesimple.online).

**Live URL:** `techmdesimple.online`
**AI Consulting branch:** `techmdesimple.online/ai-consulting`

---

## Cal.com

Booking link is set to `https://cal.com/techsimple/30min`. The inline embed is active in the booking section.

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
4. Set Custom domain: `techmdesimple.online`
5. In your DNS (Cloudflare or registrar), add these records:
   ```
   A     @  →  185.199.108.153
   A     @  →  185.199.109.153
   A     @  →  185.199.110.153
   A     @  →  185.199.111.153
   CNAME www  →  your-github-username.github.io
   ```
6. GitHub will auto-provision an SSL certificate via Let's Encrypt

**Note on AI Consulting page:** Since this repo owns the root domain, the `/ai-consulting` page
should live in an `ai-consulting/` folder inside this same repo (i.e. `ai-consulting/index.html`)
so it remains accessible at `techmdesimple.online/ai-consulting`.

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
