# 🔧 GHOST1O1 Design — Guide d'installation

---

## 📦 Méthode 1 — CDN (zero install)

```html
<link rel="stylesheet" href="https://cdn.ghost1o1.dev/design/v1.1/ghost1o1.css">
<script src="https://cdn.ghost1o1.dev/design/v1.1/ghost1o1.js" defer></script>
```

## 📦 Méthode 2 — Local (clone)

```bash
git clone https://github.com/187Ghost101/ghost1o1-design.git
cp ghost1o1-design/ghost1o1.css mon-projet/
cp ghost1o1-design/ghost1o1.js mon-projet/
```

```html
<link rel="stylesheet" href="ghost1o1.css">
<script src="ghost1o1.js" defer></script>
```

## 📦 Méthode 3 — npm (optionnel)

```bash
# Pas encore publié sur npm, en cours
# Pour l'instant utilise le CDN ou local
```

## 🐧 Démo locale

```bash
git clone https://github.com/187Ghost101/ghost1o1-design.git
cd ghost1o1-design
python3 -m http.server 8000
firefox http://localhost:8000
```

## ✅ Vérification

Ouvre la démo : `index.html` doit afficher tous les composants avec le thème NOCTURNE.

---

*"There is no lock." — ghost1o1*
