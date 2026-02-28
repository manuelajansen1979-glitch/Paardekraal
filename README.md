# 🌿 Paardekraal Guest House Website

A single-file website for Paardekraal, a self-catering guest house near Springbok in Namaqualand, Northern Cape. Built for two guests, off-grid, no signal.

---

## How to Use This

The website lives in **one file: `index.html`**. Open it in any browser to see it. No server needed, no packages, no installation.

To put it live for free, see [Hosting on GitHub Pages](#hosting-on-github-pages) below.

---

## ✏️ How to Edit Your Content

Open `index.html` in any text editor (Notepad, TextEdit, VS Code, etc.).

Every section that needs editing is marked with a `✏️ EDIT` comment in the code. Search for `✏️` to jump between them.

---

### 1. Hero Section — Top of the Page

**Find this block near the top:**

```html
<div class="hero-eyebrow">Namakwaland · Northern Cape · South Africa</div>
<h1>Paard<em>ekraal</em></h1>
<p class="hero-tagline">Where the karoo breathes and the stars belong to you</p>
<div class="hero-meta">
  <span>For 2 Guests</span>
  <span>Near Springbok</span>
  <span>Off-Grid · No Signal</span>
  <span>Self-Catering</span>
</div>
```

**What to change:**
- `hero-tagline` — your own short poetic description of the place
- `hero-meta` spans — the little badge labels (capacity, type, location)
- `hero-eyebrow` — the small text above the name

---

### 2. About Section

**Find this block (look for the `About the Farm` label):**

```html
<p>Paardekraal is a <strong>private guest house</strong> tucked into...</p>
<p>Built for two, the cottage is <strong>fully off-grid</strong>...</p>
<p>In spring, when the wildflowers bloom...</p>
```

**What to change:**
- Rewrite the three `<p>` paragraphs with your own description of the farm.
- Use `<strong>text</strong>` to make words bold.

---

### 3. Features / Amenities Grid

**Find blocks that look like this:**

```html
<div class="feature-item">
  <div class="feature-icon">🛏️</div>
  <div class="feature-name">Comfortable Bedroom</div>
  <div class="feature-desc">Queen bed with quality linen. Quiet and dark at night.</div>
</div>
```

**What to change:**
- `feature-icon` — change the emoji to anything you like (🪵 🌵 🐦 🧺 💧 etc.)
- `feature-name` — short name for the amenity
- `feature-desc` — one or two sentence description

**To add a new feature:** copy one whole `<div class="feature-item">...</div>` block and paste it inside the `features-grid` div.

**To remove a feature:** delete one whole `<div class="feature-item">...</div>` block.

---

### 4. Experience Section

**Find blocks that look like this:**

```html
<div class="exp-item">
  <div class="exp-num">01</div>
  <div>
    <div class="exp-title">Wildflower Season</div>
    <p class="exp-desc">August to October, when the Namaqualand bursts...</p>
  </div>
</div>
```

**What to change:**
- `exp-title` — name of the experience or activity
- `exp-desc` — a paragraph describing it
- Numbers (`01`, `02` etc.) can stay as is or you can update them if you add/remove items

---

### 5. Rates & Price

**Find this line:**

```html
<div class="rate-price">R ✏️ 950</div>
```

**Change `950` to your actual nightly rate.**

**Find the includes list:**

```html
<ul class="rate-includes">
  <li>Self-catering — bring your own food & drinks</li>
  <li>Linen & towels provided</li>
  ...
</ul>
```

Edit the `<li>` items to match what you include in your rate. Add or remove `<li>` lines as needed.

---

### 6. Contact Details

**Find this block:**

```html
<p>📞 <a href="tel:+27000000000">+27 00 000 0000</a></p>
<p>✉️ <a href="mailto:paardekraal@email.com">paardekraal@email.com</a></p>
```

**Change both:**
- `tel:+27000000000` → your actual phone number (no spaces, international format)
- The visible number `+27 00 000 0000` → same number, readable format
- `mailto:paardekraal@email.com` → your actual email address
- The visible email `paardekraal@email.com` → same email

---

### 7. Directions & GPS Coordinates

**Find this paragraph:**

```html
<p class="directions-text">
  Paardekraal is located approximately <strong>✏️ 15 km from Springbok</strong> on the <strong>✏️ [Road Name] road</strong>...
</p>
```

**Replace** the `✏️` placeholder text with your actual directions. Write it like you'd tell a guest on the phone.

**Find the GPS line:**

```html
<div class="coords">−29.°S  &nbsp;|&nbsp;  17.°E</div>
```

**Replace** with your actual decimal GPS coordinates, e.g.:
```html
<div class="coords">−29.6543°S  &nbsp;|&nbsp;  17.8821°E</div>
```

---

### 8. Footer Tagline

**Find:**

```html
<p><span>No signal. No rush. Just the veld.</span></p>
```

Change to your own one-liner if you prefer.

---

## 🎨 Changing Colours

All the colours are set as variables at the top of the `<style>` section:

```css
:root {
  --sand:    #f0e8d8;   /* warm sandy background */
  --stone:   #c8b89a;   /* mid-tone stone */
  --earth:   #7a5c3a;   /* earthy brown text */
  --bark:    #3d2b1a;   /* dark brown (headings, nav) */
  --sage:    #7d8c6a;   /* green-grey (features section bg) */
  --dusty:   #b5a98a;   /* muted warm beige */
  --sky:     #d4e0e8;   /* pale sky blue */
  --rust:    #9c4a28;   /* rust red (links, accents) */
  --cream:   #faf6ef;   /* off-white page background */
}
```

Change any hex code to adjust the palette. Use a tool like [coolors.co](https://coolors.co) to pick colours.

---

## 🖼️ Adding Photos (Optional)

The current site uses illustrated SVG artwork instead of photos (so it works without internet and loads instantly). If you want to add a real photo:

Find the `about-art` div and replace the SVG with an image tag:

```html
<div class="about-art">
  <img src="your-photo.jpg" alt="Paardekraal guesthouse" style="width:100%;height:380px;object-fit:cover;border-radius:2px;">
</div>
```

Put your photo file in the same folder as `index.html`.

---

## 🌐 Hosting on GitHub Pages

This is free and takes about 5 minutes:

1. Create a free account at [github.com](https://github.com)
2. Create a new repository — name it anything (e.g. `paardekraal`)
3. Upload `index.html` to the repository
4. Go to **Settings → Pages**
5. Under "Source", select **Deploy from a branch → main → / (root)**
6. Click Save
7. Your site will be live at: `https://yourusername.github.io/paardekraal`

---

## 📁 File Structure

```
paardekraal/
└── index.html        ← The entire website (everything is in here)
└── README.md         ← This guide
```

No other files needed. No dependencies. No build step.

---

## 📝 Quick Checklist Before Going Live

- [ ] Updated the phone number
- [ ] Updated the email address
- [ ] Replaced the price (R ✏️ 950)
- [ ] Written real directions
- [ ] Added real GPS coordinates
- [ ] Updated the About paragraphs with your own words
- [ ] Checked the features list matches what you actually offer
- [ ] Read through the whole site in a browser

---

*Paardekraal · Namaqualand · Northern Cape*# Paardekraal
