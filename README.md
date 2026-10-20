# cPALSs Play — inflatable carnival games

Live: [https://play.cpalss.com](https://play.cpalss.com)  
Repo: [cPALSs/play](https://github.com/cPALSs/play)

Thin public page for **underwriting and partner review**: owned Magic Jump 8-station carnival games (not bounce houses). **No public rate card.**

Staff context: [Inflatable Carnival Games proposal](../../../Operations/Festivals%20Committee/Inflatable%20Carnival%20Games/) · [Partner-operator research](../../../Operations/Festivals%20Committee/Inflatable%20Carnival%20Games/Research/Inflatable%20Carnival%20Games%20-%20Partner-Operator%20Path.md)

## Edit / preview / publish

```bash
# From this folder (Operations/Sites/play)
python3 -m http.server 8765
# → http://127.0.0.1:8765

git add -A && git commit -m "Update Play site" && git push
```

Push to `main` deploys via `.github/workflows/deploy-pages.yml`.

## Content

| Path | What |
|------|------|
| `index.html` | Copy, SKU list, org facts |
| `assets/stations/` | Manufacturer catalog photos (watermarked Magic Jump) |
| `CNAME` | `play.cpalss.com` |

Do not post rental prices, Ellie/Raul contractor terms, U-Haul unit numbers, or vault paths. CTAs are `mailto:contact@cpalss.com` only.

Replace catalog photos with **our** inflated-kit photos when those exist.

## DNS

On the **cpalss.com** zone:

| Type | Name | Value |
|------|------|--------|
| CNAME | `play` | `cpalss.github.io` |

Then GitHub repo **Settings → Pages** → custom domain `play.cpalss.com` → Enforce HTTPS.

## Rules

Visitor pages must not link monorepo paths or private vault docs. See cPALSs `.cursor/rules/github-pages-public-sites.mdc`.
