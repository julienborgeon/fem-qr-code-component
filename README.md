<p align="right" dir="ltr">
  🇫🇷 <strong>Français</strong> ·
  <a href="./README.en.md" lang="en" hreflang="en" rel="alternate" title="Read this doc in English" aria-label="Read this doc in English">English</a>
</p>

# Frontend Mentor – QR code component (solution)

[![Vite](https://img.shields.io/badge/Vite-⚡-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/) [![Tailwind CSS v4](https://img.shields.io/badge/Tailwind%20CSS-v4-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/) [![Netlify](https://img.shields.io/badge/Netlify-deploy-00C7B7?logo=netlify&logoColor=white)](https://www.netlify.com/) [![Live](https://img.shields.io/badge/Live-jb--fem--qr--code--component.netlify.app-brightgreen)](https://jb-fem-qr-code-component.netlify.app/)

Ce repo contient ma solution au défi **[QR code component](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H)** de Frontend Mentor.

> 🎯 Objectif personnel : produire un **composant accessible, sémantique et moderne**, avec une attention particulière à la typographie (polices locales, taille 1rem/16px pour la lisibilité) et à la structure HTML. Le choix des technologies (Vite + Tailwind v4) est arbitraire et a pour but de peaufiner ma maîtrise du framework.

---

## 🔎 Aperçu

### Le challenge

- Afficher une **carte** centrée avec une image de QR et du texte descriptif.
- Respecter la palette et la typo fournies (Outfit 400/700).

### Capture

![Screenshot de la solution](https://jb-fem-qr-code-component.netlify.app/og.jpg)

### Liens

- Live : [https://jb-fem-qr-code-component.netlify.app/](https://jb-fem-qr-code-component.netlify.app/)

---

## 🚀 Lancer le projet

```bash
npm install
npm run dev      # serveur local
npm run build    # build de production (dossier dist/)
npm run preview  # prévisualisation du build
```

---

## 🧱 Construit avec

- **HTML5 sémantique** (`main`, `article`, `img`)
- **Tailwind CSS v4** (tokens `@theme` : couleurs, fonts, radius)
- **Flex/Grid minimal** (centrage + respo `xs:`)
- **Polices locales WOFF2** (Outfit 400/700)
- **Vite + Netlify** (preview)

---

## 🧭 Démarche & choix d’implémentation

### Structure HTML

- **Tokens Tailwind v4** : `--color-slate-*`, `--color-accent`, `--radius-card`, `--spacing-card`, `--font-outfit` → utilitaires (`text-*`, `bg-*, rounded-*`, `p-card`, `font-outfit`).
- Liens du footer : soulignement lisible + **focus ring**.

### Design System

- Police 16x pour améliorer la lisibilité.

### Polices

- **Auto‑hébergées** dans `public/fonts`, préchargement **uniquement** des poids critiques (Outif 700/400) pour éviter les warnings _preloaded but not used quickly_; des audits web.
- `font-synthesis-weight: none` pour éviter les faux graissages.

---

## ⚡ Performance

- **Tailwind v4 JIT** → CSS minimal.
- **Polices WOFF2** + `preload` ciblé + `swap`.

> Piste à explorer : inliner le **critical CSS** via [`vite-plugin-beasties`](https://github.com/danielroe/beasties) pour gagner en FCP/LCP.

---

## 🧪 Ma démarche

### Technologies utilisées

- **Semantic HTML5 markup**
- **CSS custom properties** (via tokens Tailwind v4 dans `@theme`)
- **Mobile-first workflow**
- **Vite** (bundler/build)
- **Tailwind CSS v4**
- **Netlify** (hébergement & headers)

### Ce que j'ai appris

- Les **tokens v4** génèrent automatiquement les utilitaires (ex. `--color-accent` → `text-accent`, `bg-accent`).
- Précharger les ressources utiles **above the fold** pour éviter les warnings.

### Pistes d’amélioration

- Exporter le PNG du QR en WebP et tester `<picture>`.

### Ressources utiles

- Tailwind v4 – `@theme` & tokens : [https://tailwindcss.com/docs/theme](https://tailwindcss.com/docs/theme)
- MDN – Images responsives (`<picture>`, `srcset`, `sizes`) : [https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images](https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

---

## 👤 Auteur

- Website — [https://www.julienborgeon.fr](https://www.julienborgeon.fr)

---

## 🙌 Remerciements

Merci à **Frontend Mentor** pour le design du challenge et à la communauté pour les retours.  
Un clin d’œil aux ressources MDN & Tailwind pour la clarté de leur doc.

---

## 📁 Structure du projet

```bash
public/
  assets/
    favicon-32x32.png
    image-header-desktop.jpg
    image-header-mobile.jpg
  fonts/
    inter-v15-latin-regular.woff2
    inter-v15-latin-700.woff2
  og.jpg
src/
  main.css
.gitattributes
.gitignore
.prettierrc     → Tailwind IntelliSense + Prettier (VSC)
index.html
netlify.toml
package-lock.json
package.json
README.md
vite.config.js
```
