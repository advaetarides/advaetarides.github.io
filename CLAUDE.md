# Advaeta Rides — Website

## Links

- **YouTube**: https://www.youtube.com/@AdvaetaRides
- **Website**: https://advaetarides.github.io

## Brand

- **Name**: Advaeta Rides (two words, space between)
- **Tagline**: "A World of Adventure & Faith in Cogs & Carvings"
- **YouTube Description**: "The Journey is the Destination. We don't just count the miles; we make the miles count."
- **Content**: Cinematic travel vlogs, mindset talks, soulful journeys
- **Aesthetic**: Explorer, adventurer, steampunk-meets-heritage, carved bronze medallion
- **NOT**: Tech, blueprint, clinical, modern-minimal

## Color Palette

| Name | Hex | CSS Variable | Use |
|------|-----|-------------|-----|
| Black | #0C0C0C | --black | Background |
| Bronze | #C4944A | --bronze | Headings, buttons, accents |
| Bronze dim | #8B6914 | --bronze-dim | Borders, dates |
| Teal | #2A7B7B | --teal | Section titles, code |
| Teal light | #3AA0A0 | --teal-light | Card headings |
| Cream | #F5E6C8 | --cream | Body text |
| Muted | #8B7B5E | --muted | Secondary text, nav |
| Dark brown | #2A2015 | --dark-brown | Borders, dividers |

## Fonts

| Use | Font |
|-----|------|
| Display/titles | Cinzel Decorative |
| Headings | Cinzel |
| Body text | Cormorant Garamond |
| Tagline/accent | Uncial Antiqua |

## Site Structure

```
advaetarides.github.io/
├── index.html              ← Landing page
├── about.html              ← About page
├── blog/
│   ├── index.html          ← Blog listing
│   ├── _template.html      ← Copy this to create new articles
│   ├── three-ts.html       ← Article
│   └── fits.html           ← Article
├── tools/
│   ├── index.html          ← Tools listing
│   └── fits.html           ← FITS calculator
├── vlogs/
│   └── index.html          ← Vlog index with season tabs
├── assets/
│   ├── css/style.css       ← Shared design system (ALL pages use this)
│   ├── images/
│   │   ├── logo.png
│   │   ├── hero-art.png
│   │   └── blog/           ← Blog article images
│   └── thumbnails/         ← Vlog thumbnails
└── README.md
```

## No Build Tools

This is a pure static HTML site. No Jekyll, no Node, no build step. Push HTML files → GitHub Pages serves them. That's it.

## How to Add a New Blog Article

### 1. Copy the template
```bash
cp blog/_template.html blog/your-article-name.html
```

### 2. Edit the file
- Change `<title>` tag
- Change the date
- Change `<h1>` title
- Write content using standard HTML

### 3. Everything auto-styles

The shared CSS (`assets/css/style.css`) handles all styling. Just write HTML:

| You write | It becomes |
|-----------|-----------|
| `<h1>` | Large bronze title |
| `<h2>` | Teal section heading with bottom border |
| `<h3>` | Smaller bronze heading |
| `<p>` | Cream body text |
| `<img>` | Gold-bordered frame with shadow |
| `<blockquote>` | Teal left border, dark background |
| `<table>` | Bronze headers, hover-highlighted rows |
| `<code>` | Teal inline code |
| `<pre>` | Code block with teal left border |
| `<a>` | Bronze link, underline on hover |
| `<hr>` | Bronze gradient divider |
| `<strong>` | Bright cream emphasis |
| `<li>` | Bronze bullet/number markers |

No classes needed. No inline styles. Just semantic HTML.

### 4. Add images
```bash
# Put image in assets
cp your-image.png assets/images/blog/

# Reference in article
<img src="../assets/images/blog/your-image.png" alt="Description">
```
Images auto-get: gold border, dark background, shadow. No styling needed.

### 5. Add to blog listing

Open `blog/index.html`, add a card:
```html
<a href="your-article-name.html" style="text-decoration:none; border:none;">
  <div class="framework-card">
    <h3>Your Article Title</h3>
    <p>Short description.</p>
    <small style="color:#8B6914; font-family:var(--font-heading); letter-spacing:2px; font-size:0.65rem;">DATE</small>
  </div>
</a>
```

### 6. Push
```bash
git add .
git commit -m "Add article: Your Title"
git push
```
Live in ~1 minute.

## How to Add a New Vlog Episode

1. Add thumbnail to `assets/thumbnails/vlog-NN.png`
2. Edit `vlogs/index.html` — add a vlog card in the correct season tab
3. Link the card to the YouTube video URL
4. Push

## How to Add a New Tool

1. Create `tools/your-tool.html` (self-contained HTML+CSS+JS)
2. Add a card in `tools/index.html` linking to it
3. Tools can have their own visual style (like FITS has dark navy)
4. Push

