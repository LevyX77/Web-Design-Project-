# 🕯️ LUMIÈRE — Maison de Parfums

> *« L'art de capturer l'invisible, maintenant en ligne. »*

Application web de vente de parfums, entièrement construite en **HTML5 · CSS3 · JavaScript ES6** natif — sans framework externe.

---

## ✨ Fonctionnalités

- **Page d'accueil Hero** — grille CSS 2 colonnes avec flacon SVG animé (animation `@keyframes` CSS pure)
- **Navigation fixe** — effet glassmorphism (`backdrop-filter: blur`) et compteur de panier mis à jour dynamiquement
- **Catalogue / Collections** — grille `auto-fill` avec filtrage par famille olfactive et recherche en temps réel
- **Panier latéral** — sidebar qui glisse depuis la droite (`translateX`), gestion des quantités
- **Section Histoire** — fond sombre, cadre décoratif aux coins dorés via pseudo-éléments CSS (`::before` / `::after`)
- **Section Savoir-faire** — 4 étapes du processus de création avec apparition progressive au scroll (`IntersectionObserver`)
- **Footer & Newsletter** — grille 4 colonnes, validation email JavaScript côté client

---

## 🛠️ Stack technique

| Technologie | Détail |
|---|---|
| HTML5 | Structure sémantique |
| CSS3 | Grid, variables CSS, animations, glassmorphism |
| JavaScript ES6 | Manipulation du DOM, IntersectionObserver, gestion du panier |
| **Dépendances externes** | **Aucune** |

---

## 📁 Structure du projet

```
lumiere/
├── index.html        # Structure principale (hero, nav, catalogue, panier, footer)
├── style.css         # Variables CSS globales, grilles, animations
└── script.js         # Logique panier, filtres, IntersectionObserver, newsletter
```

---

## 🎨 Palette de couleurs

Les couleurs sont centralisées dans `:root` via des variables CSS :

```css
:root {
  --gold:       #c9a96e;  /* Or — accents, CTA */
  --cream:      #faf6f0;  /* Fond principal */
  --dark:       #1a1510;  /* Sections sombres */
  --smoke:      #f0ebe2;  /* Cartes produits */
  --text-muted: #8a7d6b;  /* Textes secondaires */
}
```

---

## 🚀 Lancer le projet

Aucune installation requise. Il suffit d'ouvrir `index.html` dans un navigateur :

```bash
# Option 1 — ouverture directe
open index.html

# Option 2 — serveur local (recommandé)
npx serve .
# ou
python3 -m http.server 8080
```

---

## 📦 Fonctionnement du panier

```js
function addToCart(id) {
  const existing = cart.find(x => x.id === id);
  if (existing) existing.qty++;
  else cart.push({ ...products.find(x => x.id === id), qty: 1 });
  updateCart();
}
```

Le panier est géré entièrement en mémoire JavaScript. Les articles sont affichés dans une sidebar latérale qui s'ouvre via `toggleCart()`.

---

## 📄 Licence

© 2025 LUMIÈRE Maison de Parfums — Document confidentiel.# Web-Design-Project-
