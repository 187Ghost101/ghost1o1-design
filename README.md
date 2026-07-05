<div align="center">

```
   ▄█████ █  ██  ▄█████ ▄█████▄  ██   ██ ▄█████ █    ██  ██ ██    ██
  ██      ██▄██  ██     ██   ██  ██▄▄▄██ ██     ██    ██  ██ ██    ██
  ██  ███ ██▀██  █████  ██████   ██   ██ █████  ██    ██  ██ ██    ██
  ██   ██ ██  ██ ██     ██   ██  ██   ██ ██      ██  ▄██  ██  ██  ██
   ▀████▀ ██  ██ ▀█████ ██   ██  ██   ██ ▀█████   ▀███▀██▄██  ▀███▀
```

![GHOST1O1](https://img.shields.io/badge/GHOST1O1-L'EVEIL_NOCTURNE-e63946?style=for-the-badge&logo=ghost&logoColor=white)
![Version](https://img.shields.io/badge/VERSION-1.1-00d4ff?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-OPERATIONAL-2ecc71?style=for-the-badge)
![Style](https://img.shields.io/badge/STYLE-AVANT_GARDE-9b59b6?style=for-the-badge)

# 🎨 GHOST1O1 DESIGN
## *Avant-Garde Hacker UI Norm*

**Design system complet pour outils de sécurité. Dark by default, brutal par design.**

[Hub](https://github.com/187Ghost101/ghost1o1) · [Demo](https://187ghost101.github.io/ghost1o1-design/) · [SECURITY](SECURITY.md)

> *Le design n'est pas cosmétique. C'est de l'ergonomie radicale.*

</div>

---

## 🔥 C'est quoi ?

GHOST1O1 DESIGN est un **design system** complet pour les outils de hacking/sécurité. Inspiré du brutalisme digital, du terminal Unix et de la culture hacker underground, il pose une **norme visuelle** pour les outils offensifs et défensifs.

**Objectif :** remplacer le Bootstrap/Material générique par une identité visuelle qui **correspond à l'audience** des outils de sécurité.

---

## ✨ Features

- **Palette nocturne** : noir profond, rouge GHOST, cyan NOCTURNE
- **Typographie mono-first** : JetBrains Mono, Fira Code
- **Composants** : panels, cards, terminals, modals, tables
- **Animations sobres** : pulse sur les status dots, transitions courtes
- **Responsive** : fonctionne du 4K au cell 360px
- **Zero dépendance** : CSS pur + 5KB de JS optionnel
- **A11y** : contraste WCAG AA minimum, focus visible

---

## 🚀 Démarrage 60 secondes

```bash
git clone https://github.com/187Ghost101/ghost1o1-design.git
cd ghost1o1-design

# Voir la démo
firefox examples/dashboard.html

# Intégrer dans ton projet
cp ghost1o1.css /ton/projet/
# Ajouter dans <head> :
# <link rel="stylesheet" href="ghost1o1.css">
```

---

## 🎨 Aperçu

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="ghost1o1.css">
</head>
<body>
  <div class="card">
    <div class="card-header">
      <h3>📡 Streams</h3>
      <span class="badge badge-red">LIVE</span>
    </div>
    <div class="card-body">
      <button class="btn btn-accent">ADD</button>
      <button class="btn btn-cyan">EXPORT</button>
    </div>
  </div>
</body>
</html>
```

→ Rendu : dashboard dark, accent rouge GHOST, typo mono, panels structurés.

---

## 🧩 Composants

| Composant | Usage |
|-----------|-------|
| `.card` / `.card-header` / `.card-body` | Conteneur de panel |
| `.btn` / `.btn-accent` / `.btn-cyan` | Boutons (4 variantes) |
| `.badge-red` / `.badge-green` / `.badge-yellow` | Status badges |
| `.terminal` | Zone output type terminal |
| `.modal` / `.modal-overlay` | Dialogues modaux |
| `.progress-bar` | Barre de progression |
| `.status-dot` | Indicateur online/offline |
| `.grid-{1,2,3,4}` | Grilles responsive |
| `.nav-item` | Items de sidebar |

---

## 🎯 Palette

| Couleur | Hex | Usage |
|---------|-----|-------|
| `--bg` | `#0a0a0f` | Background principal |
| `--bg2` | `#0f0f1a` | Cartes |
| `--bg3` | `#141428` | Inputs |
| `--accent` | `#e63946` | Action principale |
| `--green` | `#2ecc71` | Succès / LIVE |
| `--cyan` | `#00d4ff` | Info / Liens |
| `--yellow` | `#f39c12` | Warning |
| `--purple` | `#9b59b6` | Avancé |
| `--text` | `#c8c8d0` | Body |
| `--text2` | `#8888a0` | Labels |

---

## 🔤 Typographie

```css
:root {
  --font-mono: 'JetBrains Mono', 'Fira Code', 'Consolas', monospace;
  --font-sans: 'Inter', 'SF Pro', 'Segoe UI', system-ui, sans-serif;
}
```

Headers : letter-spacing: +2px, weight 700.
Body : 12-14px, line-height 1.5.

---

## 🤝 Contribution

Recherché :
- Nouveaux composants
- Thèmes alternatifs (light mode éphémère, color-blind)
- Traductions de la doc
- Exemples d'usage

📜 **[CONTRIBUTING.md](CONTRIBUTING.md)**

---

## 📜 Licence

**MIT License**

---

<div align="center">

**L'ÉVEIL NOCTURNE** · [ghost1o1](https://github.com/187Ghost101) — 2026

*There is no lock.*

</div>
