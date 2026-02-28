# Paardekraal — Namaqualand Guest House

Private off-grid guest house for two, near Springbok, Northern Cape. No signal. Just the veld.

## Deploy to Vercel

1. Copy the code below into a file called `index.html`
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Drag and drop the `index.html` file
4. Click **Deploy** — done ✓

## Edit Before Deploying

Search the code for these placeholders and replace them:

| Placeholder | Replace with |
|---|---|
| `+27 00 000 0000` | Your phone number |
| `stay@paardekraal.co.za` | Your email address |
| `R 950` | Your nightly rate |
| `[road name]` | Actual road name |
| `[landmark / gate description]` | How to find the gate |
| `−29.°S · 17.°E` | Your real GPS coordinates |

---

## Website Code

Copy everything between the fences into `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Paardekraal — Namaqualand Guest House</title>
<meta name="description" content="A private off-grid guest house for two, near Springbok in the Northern Cape. No signal. Just the veld.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;1,400;1,500&family=Outfit:wght@200;300;400&display=swap" rel="stylesheet">
<style>
:root {
  --bg:      #f7f2e8;
  --sand:    #e8dfc8;
  --stone:   #c4b49a;
  --earth:   #8b6848;
  --bark:    #2e1f0f;
  --sage:    #6b7a58;
  --rust:    #a84228;
  --dusty:   #a89878;
  --night:   #181210;
  --cream:   #fdf9f2;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { background: var(--bg); color: var(--bark); font-family: 'Outfit', sans-serif; font-weight: 300; overflow-x: hidden; }
body::after {
  content: ''; position: fixed; inset: 0; z-index: 9999; pointer-events: none;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='g'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='300' height='300' filter='url(%23g)' opacity='0.035'/%3E%3C/svg%3E");
  opacity: 0.5;
}

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 500;
  display: flex; align-items: center; justify-content: space-between;
  padding: 1.1rem 2.5rem;
  background: rgba(247,242,232,0.82); backdrop-filter: blur(14px);
  border-bottom: 1px solid rgba(196,180,154,0.35);
}
.nav-brand { font-family: 'Playfair Display', serif; font-size: 1.05rem; letter-spacing: 0.06em; color: var(--bark); text-decoration: none; }
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a { font-size: 0.68rem; letter-spacing: 0.18em; text-transform: uppercase; color: var(--earth); text-decoration: none; transition: color 0.2s; }
.nav-links a:hover { color: var(--bark); }
@media (max-width: 640px) { .nav-links { display: none; } }

/* HERO */
.hero {
  min-height: 100vh; display: flex; flex-direction: column; justify-content: flex-end;
  padding: 0 0 5rem; position: relative; overflow: hidden; background: var(--night);
}
.hero-sky { position: absolute; inset: 0; background: radial-gradient(ellipse at 60% 0%, #2a1a30 0%, #0e0a06 55%, var(--night) 100%); }
.stars {
  position: absolute; inset: 0;
  background-image:
    radial-gradient(1.5px 1.5px at 10% 15%, rgba(255,248,230,0.9) 0%, transparent 100%),
    radial-gradient(1px 1px at 25% 8%, rgba(255,248,230,0.7) 0%, transparent 100%),
    radial-gradient(2px 2px at 40% 20%, rgba(255,248,230,0.8) 0%, transparent 100%),
    radial-gradient(1px 1px at 55% 5%, rgba(255,248,230,0.6) 0%, transparent 100%),
    radial-gradient(1.5px 1.5px at 70% 12%, rgba(255,248,230,0.9) 0%, transparent 100%),
    radial-gradient(1px 1px at 85% 18%, rgba(255,248,230,0.5) 0%, transparent 100%),
    radial-gradient(2px 2px at 15% 35%, rgba(255,248,230,0.6) 0%, transparent 100%),
    radial-gradient(1px 1px at 30% 28%, rgba(255,248,230,0.8) 0%, transparent 100%),
    radial-gradient(1.5px 1.5px at 48% 40%, rgba(255,248,230,0.5) 0%, transparent 100%),
    radial-gradient(1px 1px at 62% 32%, rgba(255,248,230,0.7) 0%, transparent 100%),
    radial-gradient(2px 2px at 78% 38%, rgba(255,248,230,0.9) 0%, transparent 100%),
    radial-gradient(1px 1px at 92% 25%, rgba(255,248,230,0.6) 0%, transparent 100%),
    radial-gradient(1.5px 1.5px at 20% 45%, rgba(255,248,230,0.7) 0%, transparent 100%),
    radial-gradient(1px 1px at 35% 55%, rgba(255,248,230,0.5) 0%, transparent 100%),
    radial-gradient(2px 2px at 50% 48%, rgba(255,248,230,0.8) 0%, transparent 100%),
    radial-gradient(1px 1px at 67% 52%, rgba(255,248,230,0.6) 0%, transparent 100%),
    radial-gradient(1.5px 1.5px at 82% 44%, rgba(255,248,230,0.7) 0%, transparent 100%),
    radial-gradient(2px 2px at 22% 62%, rgba(255,248,230,0.9) 0%, transparent 100%),
    radial-gradient(1.5px 1.5px at 58% 65%, rgba(255,248,230,0.6) 0%, transparent 100%),
    radial-gradient(1px 1px at 74% 60%, rgba(255,248,230,0.5) 0%, transparent 100%),
    radial-gradient(1px 1px at 88% 68%, rgba(255,248,230,0.7) 0%, transparent 100%);
}
.milky-way { position: absolute; inset: 0; background: radial-gradient(ellipse 120% 30% at 45% 35%, rgba(180,160,220,0.06) 0%, rgba(200,180,240,0.04) 40%, transparent 70%); }
.hero-landscape { position: absolute; bottom: 0; left: 0; right: 0; width: 100%; height: 52%; }
.hero-glow { position: absolute; bottom: 45%; left: 0; right: 0; height: 80px; background: linear-gradient(to top, rgba(120,80,40,0.25), transparent); }
.hero-content { position: relative; z-index: 10; padding: 0 3rem; animation: rise 1.6s ease both; }
@keyframes rise { from { opacity:0; transform: translateY(30px); } to { opacity:1; transform: translateY(0); } }
.hero-overline { font-size: 0.65rem; letter-spacing: 0.35em; text-transform: uppercase; color: var(--stone); margin-bottom: 1.2rem; }
.hero-title { font-family: 'Playfair Display', serif; font-size: clamp(4.5rem, 13vw, 10rem); line-height: 0.88; color: var(--sand); letter-spacing: -0.02em; margin-bottom: 1.6rem; }
.hero-title em { display: block; font-style: italic; color: var(--stone); font-size: 0.65em; margin-top: 0.2em; }
.hero-sub { font-size: clamp(0.9rem, 1.8vw, 1.15rem); color: var(--dusty); font-style: italic; font-family: 'Playfair Display', serif; margin-bottom: 2.5rem; max-width: 480px; }
.hero-tags { display: flex; gap: 0.7rem; flex-wrap: wrap; }
.hero-tag { font-size: 0.64rem; letter-spacing: 0.14em; text-transform: uppercase; color: var(--stone); border: 1px solid rgba(196,180,154,0.3); padding: 0.45rem 1rem; border-radius: 30px; background: rgba(30,20,10,0.4); backdrop-filter: blur(6px); }
.scroll-cue { position: absolute; bottom: 2rem; right: 2.5rem; z-index: 10; display: flex; flex-direction: column; align-items: center; gap: 0.5rem; color: var(--dusty); font-size: 0.58rem; letter-spacing: 0.2em; text-transform: uppercase; animation: rise 2s 1s ease both; }
.scroll-line { width: 1px; height: 48px; background: linear-gradient(to bottom, var(--dusty), transparent); animation: pulse 2.2s ease-in-out infinite; }
@keyframes pulse { 0%,100%{opacity:0.35;} 50%{opacity:0.85;} }
@media (max-width: 640px) { .hero-content { padding: 0 1.5rem; } .hero { padding-bottom: 4rem; } }

/* LAYOUT */
.section { padding: 7rem 2.5rem; }
.container { max-width: 1020px; margin: 0 auto; }
.label { font-size: 0.62rem; letter-spacing: 0.3em; text-transform: uppercase; color: var(--stone); margin-bottom: 0.9rem; }
.heading { font-family: 'Playfair Display', serif; font-size: clamp(2.4rem, 5.5vw, 4rem); line-height: 1.05; letter-spacing: -0.02em; margin-bottom: 1.5rem; }
.heading em { font-style: italic; color: var(--earth); }

/* ABOUT */
#about { background: var(--cream); }
.about-wrap { display: grid; grid-template-columns: 1fr 1fr; gap: 6rem; align-items: center; margin-top: 1rem; }
@media (max-width: 760px) { .about-wrap { grid-template-columns: 1fr; gap: 3rem; } }
.about-body p { font-size: 1.02rem; line-height: 1.9; color: var(--earth); margin-bottom: 1.2rem; }
.about-body p strong { color: var(--bark); font-weight: 400; }
.about-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; margin-top: 2.5rem; }
.stat { padding: 1.2rem; border: 1px solid var(--sand); background: var(--bg); }
.stat-num { font-family: 'Playfair Display', serif; font-size: 2rem; color: var(--earth); line-height: 1; margin-bottom: 0.3rem; }
.stat-lbl { font-size: 0.72rem; letter-spacing: 0.1em; color: var(--dusty); text-transform: uppercase; }

/* AMENITIES */
#amenities { background: var(--bark); }
#amenities .label { color: var(--stone); }
#amenities .heading { color: var(--sand); }
.amenities-grid { margin-top: 3rem; display: grid; grid-template-columns: repeat(4, 1fr); border-top: 1px solid rgba(196,180,154,0.18); border-left: 1px solid rgba(196,180,154,0.18); }
@media (max-width: 860px) { .amenities-grid { grid-template-columns: repeat(2,1fr); } }
@media (max-width: 480px) { .amenities-grid { grid-template-columns: 1fr; } }
.amenity { padding: 2rem 1.6rem; border-right: 1px solid rgba(196,180,154,0.18); border-bottom: 1px solid rgba(196,180,154,0.18); transition: background 0.22s; }
.amenity:hover { background: rgba(196,180,154,0.07); }
.amenity-icon { font-size: 1.5rem; margin-bottom: 0.9rem; }
.amenity-name { font-family: 'Playfair Display', serif; font-size: 1.05rem; color: var(--sand); margin-bottom: 0.45rem; }
.amenity-desc { font-size: 0.78rem; line-height: 1.65; color: var(--dusty); }

/* WAVE */
.wave { display: block; background: var(--bark); line-height: 0; }
.wave svg { width: 100%; display: block; }

/* EXPERIENCE */
#experience { background: var(--sand); }
.exp-list { margin-top: 3rem; }
.exp-item { display: grid; grid-template-columns: 4rem 1fr; gap: 2rem; padding: 2.2rem 0; border-bottom: 1px solid var(--stone); align-items: start; }
.exp-item:first-child { border-top: 1px solid var(--stone); }
.exp-num { font-family: 'Playfair Display', serif; font-size: 2rem; color: var(--stone); line-height: 1; padding-top: 0.15rem; }
.exp-title { font-family: 'Playfair Display', serif; font-size: 1.35rem; margin-bottom: 0.5rem; color: var(--bark); }
.exp-body { font-size: 0.88rem; line-height: 1.8; color: var(--earth); }

/* BOOKING */
#booking { background: var(--cream); text-align: center; }
.rate-card { max-width: 480px; margin: 3rem auto 0; border: 1px solid var(--stone); padding: 3.5rem 3rem; background: white; position: relative; }
.rate-card::before { content: ''; position: absolute; inset: 7px; border: 1px solid rgba(196,180,154,0.35); pointer-events: none; }
.rate-amount { font-family: 'Playfair Display', serif; font-size: 4.5rem; line-height: 1; color: var(--bark); margin-bottom: 0.3rem; }
.rate-per { font-size: 0.75rem; letter-spacing: 0.2em; text-transform: uppercase; color: var(--dusty); margin-bottom: 2rem; }
.rate-list { list-style: none; margin-bottom: 2.5rem; text-align: left; }
.rate-list li { font-size: 0.87rem; padding: 0.6rem 0; border-bottom: 1px solid var(--sand); color: var(--earth); display: flex; align-items: center; gap: 0.7rem; }
.rate-list li::before { content: "✦"; color: var(--sage); font-size: 0.6rem; flex-shrink: 0; }
.contact-details { margin-top: 3rem; font-size: 0.88rem; line-height: 2.2; color: var(--earth); }
.contact-details strong { color: var(--bark); font-weight: 400; }
.contact-details a { color: var(--rust); text-decoration: none; }
.contact-details a:hover { text-decoration: underline; }

/* LOCATION */
#location { background: var(--sage); color: var(--cream); text-align: center; }
#location .label { color: rgba(253,249,242,0.55); }
#location .heading { color: var(--cream); }
#location .heading em { color: rgba(253,249,242,0.75); }
.directions { max-width: 580px; margin: 2rem auto 0; font-size: 0.95rem; line-height: 1.95; color: rgba(253,249,242,0.8); }
.directions strong { color: var(--cream); font-weight: 400; }
.gps { margin-top: 2.2rem; font-family: 'Playfair Display', serif; font-style: italic; font-size: 1.05rem; color: rgba(253,249,242,0.55); }
.signal-badge { display: inline-block; margin-top: 2rem; padding: 0.7rem 1.6rem; border: 1px solid rgba(253,249,242,0.25); border-radius: 30px; font-size: 0.7rem; letter-spacing: 0.12em; color: rgba(253,249,242,0.6); }

/* FOOTER */
footer { background: var(--night); padding: 4rem 2.5rem 3rem; text-align: center; color: var(--dusty); }
.footer-brand { font-family: 'Playfair Display', serif; font-size: 2rem; color: var(--sand); letter-spacing: 0.06em; margin-bottom: 0.6rem; }
.footer-place { font-size: 0.72rem; letter-spacing: 0.2em; text-transform: uppercase; color: var(--stone); margin-bottom: 2rem; }
.footer-line { width: 40px; height: 1px; background: var(--stone); margin: 0 auto 2rem; opacity: 0.4; }
.footer-tagline { font-family: 'Playfair Display', serif; font-style: italic; color: var(--stone); font-size: 0.95rem; }
.footer-copy { margin-top: 2.5rem; font-size: 0.65rem; letter-spacing: 0.1em; color: rgba(164,152,120,0.4); }
</style>
</head>
<body>

<nav>
  <a class="nav-brand" href="#">Paardekraal</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#amenities">The Stay</a></li>
    <li><a href="#experience">Explore</a></li>
    <li><a href="#booking">Book</a></li>
    <li><a href="#location">Find Us</a></li>
  </ul>
</nav>

<!-- ═══════════ HERO ═══════════ -->
<section class="hero">
  <div class="hero-sky"></div>
  <div class="stars"></div>
  <div class="milky-way"></div>

  <svg class="hero-landscape" viewBox="0 0 1440 420" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="gGround" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stop-color="#4a3520"/><stop offset="100%" stop-color="#1a0e08"/>
      </linearGradient>
      <linearGradient id="gMid" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stop-color="#3d2b1a"/><stop offset="100%" stop-color="#1a0e08"/>
      </linearGradient>
    </defs>
    <path d="M0,420 L0,260 Q60,230 120,200 L190,150 L260,190 L330,130 L400,175 L470,110 L540,160 L620,100 L700,155 L780,120 L860,165 L940,135 L1020,180 L1100,145 L1180,185 L1260,155 L1340,175 L1440,160 L1440,420Z" fill="#2a1810" opacity="0.9"/>
    <path d="M0,420 L0,310 Q80,285 150,265 L230,235 L310,260 L390,230 L470,255 L550,235 L630,262 L720,238 L810,268 L900,245 L990,270 L1080,252 L1170,272 L1260,255 L1360,270 L1440,258 L1440,420Z" fill="url(#gMid)"/>
    <path d="M0,420 L0,355 Q120,335 240,342 Q360,350 480,338 Q600,326 720,335 Q840,344 960,332 Q1080,320 1200,330 Q1320,340 1440,328 L1440,420Z" fill="url(#gGround)"/>
    <!-- Aloe 1 -->
    <g transform="translate(280,238)">
      <rect x="-2" y="0" width="4" height="52" fill="#1a1008"/>
      <path d="M0,0 Q-22,-16 -30,-36 Q-12,-18 0,-2Z" fill="#3d4a2a" opacity="0.8"/>
      <path d="M0,0 Q22,-16 30,-36 Q12,-18 0,-2Z" fill="#3d4a2a" opacity="0.8"/>
      <path d="M0,10 Q-18,-4 -26,-22 Q-10,-8 0,8Z" fill="#3d4a2a" opacity="0.6"/>
      <path d="M0,10 Q18,-4 26,-22 Q10,-8 0,8Z" fill="#3d4a2a" opacity="0.6"/>
      <path d="M0,18 Q-14,4 -20,-10 Q-8,2 0,16Z" fill="#7a3a18" opacity="0.7"/>
    </g>
    <!-- Aloe 2 -->
    <g transform="translate(920,242)">
      <rect x="-2" y="0" width="4" height="48" fill="#1a1008"/>
      <path d="M0,0 Q-20,-14 -28,-32 Q-11,-16 0,-2Z" fill="#3d4a2a" opacity="0.75"/>
      <path d="M0,0 Q20,-14 28,-32 Q11,-16 0,-2Z" fill="#3d4a2a" opacity="0.75"/>
      <path d="M0,8 Q-16,-2 -22,-18 Q-9,-6 0,6Z" fill="#3d4a2a" opacity="0.55"/>
      <path d="M0,8 Q16,-2 22,-18 Q9,-6 0,6Z" fill="#3d4a2a" opacity="0.55"/>
    </g>
    <!-- Aloe 3 -->
    <g transform="translate(1200,248)">
      <rect x="-1.5" y="0" width="3" height="40" fill="#1a1008"/>
      <path d="M0,0 Q-15,-10 -20,-24 Q-8,-12 0,-1Z" fill="#3d4a2a" opacity="0.7"/>
      <path d="M0,0 Q15,-10 20,-24 Q8,-12 0,-1Z" fill="#3d4a2a" opacity="0.7"/>
    </g>
    <!-- Boulders -->
    <ellipse cx="120" cy="355" rx="90" ry="35" fill="#3a2818" opacity="0.9"/>
    <ellipse cx="108" cy="348" rx="72" ry="24" fill="#2e1f10" opacity="0.9"/>
    <ellipse cx="680" cy="360" rx="110" ry="38" fill="#3a2818" opacity="0.8"/>
    <ellipse cx="670" cy="352" rx="88" ry="26" fill="#2e1f10" opacity="0.8"/>
    <ellipse cx="1320" cy="358" rx="95" ry="32" fill="#3a2818" opacity="0.85"/>
  </svg>

  <div class="hero-glow"></div>
  <div class="hero-content">
    <div class="hero-overline">Northern Cape · South Africa · Near Springbok</div>
    <h1 class="hero-title">Paardekraal<em>Guest House</em></h1>
    <p class="hero-sub">A private off-grid retreat for two, where the karoo sky takes your breath away</p>
    <div class="hero-tags">
      <span class="hero-tag">2 Guests</span>
      <span class="hero-tag">Self-Catering</span>
      <span class="hero-tag">Off-Grid · Solar</span>
      <span class="hero-tag">No Cell Signal</span>
      <span class="hero-tag">Namaqualand</span>
    </div>
  </div>
  <div class="scroll-cue"><span>Scroll</span><div class="scroll-line"></div></div>
</section>

<!-- ═══════════ ABOUT ═══════════ -->
<section id="about" class="section">
  <div class="container">
    <div class="about-wrap">
      <div class="about-body">
        <div class="label">About the Place</div>
        <h2 class="heading">Stillness in the<br><em>ancient veld</em></h2>
        <p>Paardekraal is a <strong>private guest house</strong> nestled in the ancient landscape of Namaqualand, a short drive from Springbok in the Northern Cape. Here, the silence is total and the light is like nowhere else in South Africa.</p>
        <p>Built and kept for two, the cottage is entirely <strong>off the grid</strong> — solar powered, no Wi-Fi, no cell signal. The only thing on the schedule is whatever the land asks of you.</p>
        <p>In wildflower season, the surrounding veld turns into one of nature's great spectacles. Any time of year, the night sky rewards those who look up.</p>
        <div class="about-stats">
          <div class="stat"><div class="stat-num">2</div><div class="stat-lbl">Max Guests</div></div>
          <div class="stat"><div class="stat-num">0</div><div class="stat-lbl">Cell Bars</div></div>
          <div class="stat"><div class="stat-num">∞</div><div class="stat-lbl">Stars Visible</div></div>
          <div class="stat"><div class="stat-num">100%</div><div class="stat-lbl">Off-Grid Solar</div></div>
        </div>
      </div>

      <!-- Daytime veld illustration -->
      <svg viewBox="0 0 460 400" xmlns="http://www.w3.org/2000/svg" style="width:100%">
        <defs>
          <radialGradient id="daysky" cx="60%" cy="25%" r="70%">
            <stop offset="0%" stop-color="#e8dcc8"/>
            <stop offset="60%" stop-color="#d4c8b0"/>
            <stop offset="100%" stop-color="#c8b898"/>
          </radialGradient>
          <radialGradient id="sunglow" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stop-color="#f4d888" stop-opacity="0.8"/>
            <stop offset="100%" stop-color="#f4d888" stop-opacity="0"/>
          </radialGradient>
        </defs>
        <rect width="460" height="400" fill="url(#daysky)"/>
        <circle cx="340" cy="75" r="55" fill="url(#sunglow)"/>
        <circle cx="340" cy="75" r="26" fill="#f8e090" opacity="0.85"/>
        <path d="M0,300 Q50,265 100,245 L170,195 L245,250 L310,205 L380,248 L460,220 L460,400 L0,400Z" fill="#b8a888" opacity="0.55"/>
        <path d="M0,330 Q80,305 150,290 L220,260 L290,285 L360,265 L430,285 L460,272 L460,400 L0,400Z" fill="#8b6848" opacity="0.55"/>
        <path d="M0,365 Q115,348 230,354 Q345,360 460,349 L460,400 L0,400Z" fill="#7d8c5a"/>
        <ellipse cx="75" cy="375" rx="75" ry="30" fill="#c4b49a"/>
        <ellipse cx="72" cy="368" rx="60" ry="20" fill="#b0a088"/>
        <ellipse cx="390" cy="378" rx="65" ry="28" fill="#c4b49a"/>
        <ellipse cx="386" cy="371" rx="52" ry="18" fill="#b0a088"/>
        <path d="M210,355 L225,330 L238,340 L250,325 L262,345 L255,358 L218,360Z" fill="#e8dfc8"/>
        <!-- Aloe centre -->
        <g transform="translate(185,295)">
          <rect x="-3" y="0" width="5" height="70" fill="#2e1f0f"/>
          <path d="M1,0 Q-24,-20 -34,-46 Q-14,-22 1,-3Z" fill="#6b7a48"/>
          <path d="M1,0 Q26,-20 36,-46 Q16,-22 1,-3Z" fill="#6b7a48"/>
          <path d="M1,12 Q-20,-6 -28,-30 Q-10,-10 1,10Z" fill="#6b7a48" opacity="0.75"/>
          <path d="M1,12 Q22,-6 30,-30 Q12,-10 1,10Z" fill="#6b7a48" opacity="0.75"/>
          <path d="M1,22 Q-16,4 -22,-14 Q-8,2 1,20Z" fill="#a84228" opacity="0.8"/>
          <path d="M1,22 Q18,4 24,-14 Q10,2 1,20Z" fill="#a84228" opacity="0.8"/>
        </g>
        <!-- Aloe right -->
        <g transform="translate(310,315)">
          <rect x="-2" y="0" width="4" height="50" fill="#2e1f0f"/>
          <path d="M0,0 Q-16,-12 -22,-30 Q-9,-14 0,-2Z" fill="#6b7a48"/>
          <path d="M0,0 Q16,-12 22,-30 Q9,-14 0,-2Z" fill="#6b7a48"/>
          <path d="M0,10 Q-13,-2 -18,-18 Q-7,-4 0,8Z" fill="#6b7a48" opacity="0.7"/>
          <path d="M0,10 Q13,-2 18,-18 Q7,-4 0,8Z" fill="#6b7a48" opacity="0.7"/>
        </g>
        <!-- Cottage -->
        <rect x="38" y="315" width="55" height="35" fill="#e8dfc8"/>
        <path d="M34,317 L65,295 L96,317Z" fill="#b8a078"/>
        <rect x="50" y="330" width="12" height="20" fill="#8b6848" opacity="0.6"/>
        <rect x="68" y="322" width="10" height="10" fill="#8b6848" opacity="0.4"/>
      </svg>
    </div>
  </div>
</section>

<!-- ═══════════ AMENITIES ═══════════ -->
<section id="amenities" class="section">
  <div class="container">
    <div class="label">What's Included</div>
    <h2 class="heading" style="color:var(--sand)">Everything you <em style="color:var(--stone)">need</em></h2>
    <div class="amenities-grid">
      <div class="amenity"><div class="amenity-icon">🛏️</div><div class="amenity-name">Queen Bedroom</div><div class="amenity-desc">Comfortable queen bed, quality linen, blackout curtains. Quiet enough to hear the wind.</div></div>
      <div class="amenity"><div class="amenity-icon">🍳</div><div class="amenity-name">Equipped Kitchen</div><div class="amenity-desc">Gas stove, fridge, pots, crockery — fully stocked. Bring your own groceries.</div></div>
      <div class="amenity"><div class="amenity-icon">🔥</div><div class="amenity-name">Braai & Fire Pit</div><div class="amenity-desc">Outdoor braai area with firewood provided. Evenings under the open sky.</div></div>
      <div class="amenity"><div class="amenity-icon">🚿</div><div class="amenity-name">Hot Shower</div><div class="amenity-desc">Gas geyser for reliable hot water. Full bathroom with basin and toilet.</div></div>
      <div class="amenity"><div class="amenity-icon">☀️</div><div class="amenity-name">Solar Power</div><div class="amenity-desc">Fully off-grid solar system. Lights, charging, fridge — all covered.</div></div>
      <div class="amenity"><div class="amenity-icon">🌿</div><div class="amenity-name">Private Garden</div><div class="amenity-desc">Enclosed garden with indigenous succulents and koppie views.</div></div>
      <div class="amenity"><div class="amenity-icon">📵</div><div class="amenity-name">True Digital Detox</div><div class="amenity-desc">No Wi-Fi. No cell signal. Just presence, quiet, and whatever you brought to read.</div></div>
      <div class="amenity"><div class="amenity-icon">🌌</div><div class="amenity-name">Dark Sky Nights</div><div class="amenity-desc">Zero light pollution. The Milky Way every clear night.</div></div>
    </div>
  </div>
</section>

<!-- Wave divider -->
<div class="wave"><svg viewBox="0 0 1440 80" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg"><path d="M0,0 L0,40 Q180,80 360,55 Q540,30 720,55 Q900,80 1080,55 Q1260,30 1440,50 L1440,0Z" fill="#e8dfc8"/></svg></div>

<!-- ═══════════ EXPERIENCE ═══════════ -->
<section id="experience" class="section">
  <div class="container">
    <div class="label">Explore the Region</div>
    <h2 class="heading">What draws people<br><em>back</em></h2>
    <div class="exp-list">
      <div class="exp-item">
        <div class="exp-num">01</div>
        <div>
          <div class="exp-title">Wildflower Season</div>
          <p class="exp-body">August through October, the Namaqualand becomes one of the world's great natural spectacles. Vast carpets of orange, white and yellow daisies blanket the plains. Paardekraal is perfectly placed to follow the flower routes each morning as the blooms open with the sun.</p>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-num">02</div>
        <div>
          <div class="exp-title">Koppie Walks & Veld Wandering</div>
          <p class="exp-body">Step straight from the door into quartz fields and ancient granite outcrops. No trails needed — just walk. You'll find succulents hidden in rock crevices, lizards on warm boulders, and the peculiar silence of land that hasn't changed in centuries.</p>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-num">03</div>
        <div>
          <div class="exp-title">Springbok Town & Goegap Reserve</div>
          <p class="exp-body">A short drive takes you to Springbok for supplies, the Blue Mine lookout, and the Goegap Nature Reserve — home to springbok, gemsbok, and hundreds of succulent species. Stock up before returning to the quiet of Paardekraal.</p>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-num">04</div>
        <div>
          <div class="exp-title">Stargazing Without Distraction</div>
          <p class="exp-body">With no light pollution and no phone screen to pull you back, the night sky becomes immersive. The Southern Cross, Scorpius, the Magellanic Clouds. Lie on your back on the stoep and just look up. There is nothing else to do.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════ BOOKING ═══════════ -->
<section id="booking" class="section">
  <div class="container">
    <div class="label" style="text-align:center">Rates & Reservations</div>
    <h2 class="heading" style="text-align:center">Book your stay</h2>
    <div class="rate-card">
      <div class="rate-amount">R 950</div>
      <div class="rate-per">per night · up to 2 guests</div>
      <ul class="rate-list">
        <li>Self-catering — bring your own food &amp; drinks</li>
        <li>Linen and towels included</li>
        <li>Firewood for the braai included</li>
        <li>2-night minimum stay preferred</li>
        <li>Pets welcome by prior arrangement</li>
      </ul>
    </div>
    <div class="contact-details">
      <p><strong>To make a reservation, contact us directly:</strong></p>
      <p>📞 <a href="tel:+27000000000">+27 00 000 0000</a></p>
      <p>✉️ <a href="mailto:stay@paardekraal.co.za">stay@paardekraal.co.za</a></p>
      <p>WhatsApp preferred — we check messages when in town.</p>
      <br>
      <p style="font-size:0.78rem;color:var(--stone)">There is no signal at the property. We respond when connectivity allows.</p>
    </div>
  </div>
</section>

<!-- ═══════════ LOCATION ═══════════ -->
<section id="location" class="section">
  <div class="container">
    <div class="label">Getting Here</div>
    <h2 class="heading">Find <em>Paardekraal</em></h2>
    <p class="directions">
      Paardekraal is situated approximately <strong>15 km from Springbok</strong> on the <strong>[road name] road</strong>.
      Turn off at the <strong>[landmark / gate description]</strong> — look for the white signpost.
      <br><br>
      A standard vehicle manages the dirt road in dry conditions.
      <strong>Download offline maps before leaving Springbok</strong> — there is no connectivity beyond the N7.
      We recommend arriving before sunset on your first visit.
    </p>
    <div class="gps">−29.°S &nbsp;·&nbsp; 17.°E</div>
    <div><span class="signal-badge">📵 &nbsp; No cell signal at the property — download offline maps before arrival</span></div>
  </div>
</section>

<!-- ═══════════ FOOTER ═══════════ -->
<footer>
  <div class="footer-brand">Paardekraal</div>
  <div class="footer-place">Namaqualand · Northern Cape · South Africa</div>
  <div class="footer-line"></div>
  <div class="footer-tagline">No signal. No rush. Just the veld.</div>
  <div class="footer-copy">© 2025 Paardekraal Guest House</div>
</footer>

</body>
</html>
```
