# GHOST1O1 Design System — v1.1 NOCTURNE

> The norm for avant-garde hacker UIs. Established by **ghost1o1**.

## Install

```html
<link rel="stylesheet" href="ghost1o1.css">
<script src="ghost1o1.js"></script>
<script>G1.init();</script>
```

## What's inside

- **2 files** · `ghost1o1.css` (16KB) · `ghost1o1.js` (8KB)
- **0 dependencies** · no jQuery, no React, no Vue, no CDN
- **Design tokens** · colors, fonts, radii, glows
- **22 component classes** · cards, tags, buttons, forms, tables, terminal
- **5-layer signature system** · GHOST1O1 anchored deep & visible
- **3 auto-effects** · particles, cursor glow, 3D tilt
- **3 backgrounds** · aurora, grid, watermark

## Signature layers (deep & visible)

| Layer | Class | Where |
|-------|-------|-------|
| 1. Watermark bg | `.g1-watermark` `.g1-watermark.deep` | Repeating across screen |
| 2. Brand mark | `.g1-mark` `.g1-mark.sm/lg/xl/xxl` | Nav, headers, auth |
| 3. Sig block | `.g1-sig-block` | Splash, about, hero |
| 4. Sig inline | `.g1-sig-inline` | Topbar, footer, cards |
| 5. Sig glow | `.g1-sig-glow` | Hero areas, dramatic intros |

## Color palette

```
--g1-void:    #05050d   background
--g1-blood:   #e3063e   primary accent (red)
--g1-violet:  #a855f7   secondary
--g1-cyan:    #00f3ff   tertiary
--g1-magenta: #ec4899   quaternary
--g1-neon:    #00ff9d   success
--g1-gold:    #fbbf24   warning
```

## Quick start

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="ghost1o1.css">
</head>
<body class="g1-body">
  <div class="g1-topbar">
    <div class="g1-mark"></div>
    <span class="g1-sig-inline">GHOST1O1</span>
  </div>

  <div class="g1-card glow-violet" data-g1-tilt>
    <div class="g1-card-head"><h3><span class="g1-dot"></span>Card Title</h3></div>
    <p class="g1-muted">Card content goes here.</p>
    <button class="g1-btn blood">ACTION</button>
  </div>

  <footer class="g1-footer">
    <span class="g1-sig-inline">GHOST1O1</span> ·
    <span class="quote">"There is no lock."</span>
  </footer>

  <script src="ghost1o1.js"></script>
  <script>G1.init();</script>
</body>
</html>
```

## License

MIT — Educational use. © 2026 ghost1o1.
