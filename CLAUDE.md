# Advaeta Rides — Website

## What This Is

Static website for the Advaeta Rides motorcycle vlog channel. Hosted on GitHub Pages.

## Links

- **YouTube**: https://www.youtube.com/@AdvaetaRides
- **Website**: https://advaetarides.github.io (once deployed)

## Brand

- **Name**: Advaeta Rides (two words, space between)
- **Tagline**: "A World of Adventure & Faith in Cog & Carving"
- **YouTube Description**: "The Journey is the Destination. We don't just count the miles; we make the miles count."
- **Content**: Cinematic travel vlogs, mindset talks, soulful journeys
- **Aesthetic**: Explorer, adventurer, steampunk-meets-heritage, carved bronze medallion
- **NOT**: Tech, blueprint, clinical, modern-minimal

## Color Palette

| Name | Hex | CSS Variable | Use |
|------|-----|-------------|-----|
| Black | #0C0C0C | --black | Background |
| Bronze | #C4944A | --bronze | Headings, buttons, links, accents |
| Bronze dim | #8B6914 | --bronze-dim | Borders, dates, subtle accents |
| Teal | #2A7B7B | --teal | Section titles, code blocks, texture |
| Teal light | #3AA0A0 | --teal-light | Card headings, highlights |
| Cream | #F5E6C8 | --cream | Body text |
| Muted | #8B7B5E | --muted | Secondary text, nav links |
| Dark brown | #2A2015 | --dark-brown | Borders, dividers |

## Fonts

| Use | Font | CSS Variable |
|-----|------|-------------|
| Display/titles | Cinzel Decorative | --font-display |
| Headings | Cinzel | --font-heading |
| Body text | Cormorant Garamond | --font-body |
| Tagline/accent | Uncial Antiqua | --font-accent |

## Site Structure

```
advaetarides.github.io/
├── index.html                ← Landing page
├── blog/
│   ├── index.html            ← Blog listing
│   ├── three-ts.html         ← Three T's article
│   └── fits.html             ← FITS article
├── tools/
│   ├── index.html            ← Tools listing
│   └── fits.html             ← FITS interactive calculator
├── vlogs/
│   └── index.html            ← Vlog index
├── assets/
│   ├── css/style.css         ← Shared design system
│   └── images/
│       ├── logo.png          ← Medallion logo
│       └── blog/             ← Blog images
└── README.md
```

## Rules

- All pages use shared CSS: `assets/css/style.css`
- Every page includes the fog-layer div and consistent nav bar
- Images auto-style (gold border, shadow) — no manual styling needed
- Nav links: Home, Tools, Blog, Vlogs
- No Jekyll build required — pure static HTML
- Images from vlog production go in `assets/images/blog/`
- The FITS tool (`tools/fits.html`) has its own dark navy design — intentionally different from the main site

## Writing New Content

See README.md for article template and publishing instructions.

## Related Projects

- Vlog production files: `~/llm-kb/advaetaRides/vlogs/`
- Vlog production guide: `~/llm-kb/advaetaRides/vlogs/CLAUDE.md`
- FITS framework source: `~/llm-kb/advaetaRides/vlogs/vlog-03-fits/fits-framework.md`
