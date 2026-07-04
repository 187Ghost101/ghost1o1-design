# 🎨 GHOST1O1 Design System v1.1

> **"There is no lock."** — **ghost1o1**

Le **design system normatif** pour interfaces hacker/cyberpunk avant-gardistes. CSS + JS partagés, 0 dépendance, 22 composants, 5-layer signature system.

```
GHOST1O1 Design System v1.1
   ╔═══════════════════════════════════════╗
   ║  22 COMPONENTS · 5-LAYER SIGNATURE   ║
   ║  0 CDN · 0 DEPS · 100% LOCAL         ║
   ╚═══════════════════════════════════════╝
```

## ⚡ Aperçu

| Spec | Valeur |
|------|--------|
| **Version** | 1.1 |
| **CSS** | 34 KB (465 lignes) |
| **JS** | 10 KB (239 lignes) |
| **Dépendances** | 0 |
| **CDN** | 0 |
| **Télémétrie** | 0 |
| **Compatibilité** | Chrome 90+ / Firefox 88+ / Safari 14+ / Edge 90+ |

## 🎨 Palette

```css
--g1-void:    #05050d   /* background */
--g1-blood:   #e3063e   /* primary red */
--g1-violet:  #a855f7   /* secondary */
--g1-cyan:    #00f3ff   /* tertiary */
--g1-magenta: #ec4899   /* quaternary */
--g1-neon:    #00ff9d   /* success */
--g1-gold:    #fbbf24   /* warning */
```

## 🏷️ Signature GHOST1O1 — 5 couches

1. **Watermark bg** — texte `GHOST1O1` répété (`.09` opacity, drift 60s)
2. **Corner stamp** — vertical bottom-right "GHOST1O1 · NOCTURNE" pulsé
3. **Brand mark** — conic-gradient square (hue-rotate)
4. **Sig block** — About + splash (mark + sig-glow + quote)
5. **Sig inline** — topbar, footer, cards

## 🧩 22 composants

### Layout
- `.g1-shell` — flex shell (sidebar + content)
- `.g1-sidebar` — nav gauche
- `.g1-content` — main scrollable
- `.g1-topbar` — header sticky
- `.g1-footer` — footer bottom
- `.g1-page` — page panel

### Cards
- `.g1-card` — glass card
- `.g1-card-head` — header
- `.g1-card.glow-blood` — blood glow
- `.g1-card.glow-violet` — violet glow
- `.g1-card.glow-cyan` — cyan glow
- `.g1-card.kpi` — KPI tile

### Buttons
- `.g1-btn` — base
- `.g1-btn.blood` — red action
- `.g1-btn.violet` — violet
- `.g1-btn.cyan` — cyan
- `.g1-btn.neon` — neon
- `.g1-btn.sm` — small

### Forms
- `.g1-input` — text/number
- `.g1-select` — dropdown
- `.g1-label` — form label
- `.g1-checkbox` — checkbox

### Signature
- `.g1-mark` — brand mark
- `.g1-mark.sm` / `.lg` / `.xl` / `.xxl`
- `.g1-sig-inline` — inline text
- `.g1-sig-block` — block centered
- `.g1-sig-glow` — glowing hero
- `.g1-sig-stamp` — corner stamp

### Status
- `.g1-status` — status dot
- `.g1-tag` — tag pill
- `.g1-progress` — progress bar
- `.g1-toast` — notification

## ⚡ Auto-effects (JS)

```javascript
G1.init({
  watermarkDeep: true,
  watermarkText: 'GHOST1O1',
  watermarkCount: 8,
  particles: true,
  cursorGlow: true,
  tilt3d: true,
  toastPosition: 'top-right'
});
```

3 effects auto :
- **Particles** — floating dots (canvas)
- **Cursor glow** — gradient qui suit la souris
- **3D tilt** — perspective sur cards

## 📦 Installation

```bash
# Clone
git clone https://github.com/187Ghost101/ghost1o1-design.git
cd ghost1o1-design

# Copier dans ton projet
cp ghost1o1.css /path/to/your/project/
cp ghost1o1.js /path/to/your/project/
```

### Dans ton HTML

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="ghost1o1.css">
</head>
<body class="g1-body">
  <div class="g1-shell">
    <aside class="g1-sidebar">
      <div class="g1-nav active">Home</div>
    </aside>
    <main class="g1-content">
      <div class="g1-card glow-violet">
        <h2>Hello GHOST1O1</h2>
      </div>
    </main>
  </div>
  <script src="ghost1o1.js"></script>
  <script>G1.init();</script>
</body>
</html>
```

## 📖 Exemples

### Card simple
```html
<div class="g1-card">
  <div class="g1-card-head">
    <h3>Title</h3>
  </div>
  <p>Content here</p>
</div>
```

### KPI grid
```html
<div class="g1-grid g1-cols-4">
  <div class="g1-card kpi">
    <div class="v">42</div>
    <div class="l">Active</div>
  </div>
  ...
</div>
```

### Signature block
```html
<div class="g1-card glow-violet" style="text-align:center;padding:40px">
  <div class="g1-mark xxl" style="margin:0 auto 16px"></div>
  <div class="g1-sig-glow">GHOST1O1</div>
  <div class="g1-sig-block">
    <div class="sub">MY PROJECT v1.0 · NOCTURNE</div>
    <div class="quote">"There is no lock."</div>
  </div>
</div>
```

### Page navigation
```html
<section class="g1-page active" id="g1-page-home">
  <div class="g1-page-head">
    <h1 class="g1-page-title">Home</h1>
    <div class="g1-page-sub">Subtitle</div>
  </div>
</section>
```

```javascript
function ui(page) {
  document.querySelectorAll('.g1-page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('[data-g1-page]').forEach(n => n.classList.remove('active'));
  document.getElementById('g1-page-' + page)?.classList.add('active');
  document.querySelector(`[data-g1-page="${page}"]`)?.classList.add('active');
}
```

### Toast
```javascript
G1.toast('Hello!', 'ok');   // success
G1.toast('Error', 'err');   // error
G1.toast('Warning', 'warn'); // warning
G1.toast('Info', 'info');   // info
```

## 🎨 Personnalisation

### Override couleurs

```css
:root {
  --g1-blood: #ff5500;  /* override red */
  --g1-cyan: #00ddff;   /* override cyan */
}
```

### Désactiver particules

```javascript
G1.init({ particles: false });
```

### Watermark custom

```javascript
G1.init({
  watermarkText: 'MON_PROJET',
  watermarkCount: 12
});
```

## 📂 Structure

```
ghost1o1-design/
├── ghost1o1.css       # 34 KB — design system
├── ghost1o1.js        # 10 KB — JS shared
├── README.md          # ce fichier
└── examples/          # (à venir) demos
```

## 🏷️ Projets utilisant GHOST1O1 Nocturne

- [biobypass](https://github.com/187Ghost101/biobypass) — BioBypass Pro v11.0
- [ghosteye](https://github.com/187Ghost101/ghosteye) — GHOSTEYE v12.0
- [ycc365-ghost](https://github.com/187Ghost101/ycc365-ghost) — Cloud camera audit
- [phishcloner-ultimate](https://github.com/187Ghost101/phishcloner-ultimate) — AiTM C2
- [quebec-ultimate](https://github.com/187Ghost101/quebec-ultimate) — OSIN Chain

## 📜 License

MIT-style — usage éducatif.

---

**© 2026 ghost1o1 · GHOST1O1 Nocturne v1.1**
