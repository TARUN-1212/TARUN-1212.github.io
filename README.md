# Sai Tarun Baratam — Portfolio

Personal portfolio site for [TARUN-1212.github.io](https://tarun-1212.github.io)

Hardware security researcher in post-quantum cryptography, side-channel analysis, and FPGA/ASIC design.

## Features

- BIOS boot loader on first visit
- Interactive terminal (type `help`)
- Animated hex grid background
- Threat model diagram (animated SVG)
- Vertical publication timeline
- Research impact stats (h-index, citations)
- "Currently working on" live section
- Collaborators & Awards sections
- CV download button
- Scroll progress bar
- Google Sheets data integration

## Run locally

```bash
cd /mnt/ssd/projects/portfolio
python3 -m http.server 8080
# open http://localhost:8080
```

## Google Sheets Setup

Sheet ID: `1cZt_4LQ8danJsrh3SxbzB-aF95euMnvhUcEWb8jdrFI`

### Step 1 — Publish the sheet

`File → Share → Publish to web → Entire Document → CSV → Publish`

### Step 2 — Create these tabs with exact names and columns

**Tab: `About`**
| key | value |
|-----|-------|
| name | Sai Tarun Baratam |
| email | your@email.com |
| linkedin | your-linkedin-slug |
| scholar | your-google-scholar-id |
| cv_url | https://link-to-your-cv.pdf |
| paper_count | 8 |
| citations | 42 |
| h_index | 4 |
| project_count | 6 |

**Tab: `Papers`**
| year | venue | title | authors | abstract | pdf_url | doi_url | slides_url | code_url |

**Tab: `Projects`**
| icon | name | description | tags | github_url |
- `tags` = comma-separated: `VHDL,Vivado,NTT`

**Tab: `Collaborators`**
| institution | url |

**Tab: `Awards`**
| year | icon | title | event | description |
- `icon` = emoji: 🏆 🥈 🎓

**Tab: `CurrentWork`**
| item | status |

### Step 3 — Push & deploy

```bash
git init
git add .
git commit -m "portfolio"
git remote add origin https://github.com/TARUN-1212/TARUN-1212.github.io
git push -u origin main
```

Enable GitHub Pages: `Settings → Pages → main branch → root`

Live at: `https://tarun-1212.github.io`

## Customize

| What | Where |
|------|-------|
| Colors | `:root` CSS variables in `index.html` |
| Terminal commands | `TERM_CMDS` object in JS |
| Fallback data | `FALLBACK` object in JS |
| Threat model diagram | `#threat-svg` SVG element |
