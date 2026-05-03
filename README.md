# Advaeta Rides — Website

> A World of Adventure & Faith in Cogs & Carvings

## Structure

```
advaetarides.github.io/
├── preview.html              ← Landing page (rename to index.html before deploying)
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
│   ├── css/style.css         ← Shared design system (all pages use this)
│   └── images/
│       ├── logo.png          ← Medallion logo
│       └── blog/             ← Blog article images
├── _posts/                   ← Markdown source files (for reference, not served)
└── README.md                 ← This file
```

## How to Write a New Blog Article

### 1. Create the HTML file

Copy an existing article (e.g., `blog/three-ts.html`) and save as `blog/your-article-name.html`.

### 2. Follow this template

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Your Title — Advaeta Rides</title>
<link rel="stylesheet" href="../assets/css/style.css">
</head>
<body>
<div class="fog-layer"></div>
<nav>
  <div class="nav-left">
    <div class="nav-logo"><img src="../assets/images/logo.png" alt=""></div>
    <a href="../preview.html" class="nav-brand">Advaeta Rides</a>
  </div>
  <div class="nav-links">
    <a href="../preview.html">Home</a>
    <a href="../tools/">Tools</a>
    <a href="./">Blog</a>
    <a href="../vlogs/">Vlogs</a>
  </div>
</nav>

<main style="max-width:720px; margin:0 auto; padding:40px 24px 80px;">
  <a href="./" style="font-size:0.75rem; color:#8B7B5E; letter-spacing:2px;">← BACK TO BLOG</a>
  <small style="display:block; color:#8B6914; font-family:'Cinzel',serif; letter-spacing:2px; font-size:0.65rem; margin:12px 0 30px;">YOUR DATE HERE</small>

  <h1>Your Article Title</h1>

  <!-- Write your content here using standard HTML -->
  <p>Your paragraph text...</p>

  <h2>Section Heading</h2>
  <p>More content...</p>

  <!-- Images auto-style with gold border -->
  <img src="../assets/images/blog/your-image.png" alt="Description">

  <!-- Blockquotes get teal left border -->
  <blockquote><p>A quote or callout.</p></blockquote>

  <!-- Tables auto-style with bronze headers -->
  <table>
    <tr><th>Column 1</th><th>Column 2</th></tr>
    <tr><td>Data</td><td>Data</td></tr>
  </table>

  <!-- Code blocks get teal styling -->
  <code>inline code</code>

  <!-- Horizontal rules get bronze gradient -->
  <hr>

</main>

<footer><p>Advaeta Rides — The Journey Continues</p></footer>
</body>
</html>
```

### 3. Add images

Put images in `assets/images/blog/` and reference them as:
```html
<img src="../assets/images/blog/your-image.png" alt="Description">
```

Images automatically get a gold border, dark background, and shadow. No manual styling needed.

### 4. Add to blog index

Open `blog/index.html` and add a new card:
```html
<a href="your-article-name.html" style="text-decoration:none; border:none;">
  <div class="framework-card">
    <h3>Your Article Title</h3>
    <p>Short description of the article.</p>
    <small style="color:#8B6914; font-family:var(--font-heading); letter-spacing:2px; font-size:0.65rem;">DATE HERE</small>
  </div>
</a>
```

### 5. Push to GitHub

```bash
cd advaetarides.github.io
git add .
git commit -m "Add new article: Your Title"
git push
```

Site updates automatically in ~1 minute.

## Auto-Styled Elements

The shared CSS (`assets/css/style.css`) auto-styles everything. Just use standard HTML:

| Element | What it looks like |
|---------|-------------------|
| `<h1>` | Large bronze Cinzel Decorative font |
| `<h2>` | Teal Cinzel font with bottom border |
| `<h3>` | Smaller bronze Cinzel font |
| `<p>` | Cream Cormorant Garamond body text |
| `<img>` | Gold border frame, dark background, shadow |
| `<blockquote>` | Teal left border, dark teal background |
| `<table>` | Bronze headers, hover highlight rows |
| `<code>` | Teal background, teal text |
| `<pre>` | Code block with teal left border |
| `<a>` | Bronze text, underline on hover |
| `<hr>` | Bronze gradient line |
| `<strong>` | Bright cream |
| `<li>::marker` | Bronze bullet/number |

## Deploying to GitHub Pages

1. Create repo `advaetarides.github.io` on GitHub
2. Rename `preview.html` to `index.html`
3. Push:
```bash
cd advaetarides.github.io
git init
git add .
git commit -m "Initial site"
git remote add origin git@github.com:YOURUSERNAME/advaetarides.github.io.git
git push -u origin main
```
4. Go to repo Settings → Pages → Source: main branch, root folder
5. Site live at `https://YOURUSERNAME.github.io/`

## Color Palette

| Name | Hex | Use |
|------|-----|-----|
| Black | `#0C0C0C` | Background |
| Bronze | `#C4944A` | Headings, buttons, accents |
| Bronze dim | `#8B6914` | Borders, dates |
| Teal | `#2A7B7B` | Section titles, code |
| Teal light | `#3AA0A0` | Card headings |
| Cream | `#F5E6C8` | Body text |
| Muted | `#8B7B5E` | Secondary text, nav links |
| Dark brown | `#2A2015` | Borders, subtle lines |
