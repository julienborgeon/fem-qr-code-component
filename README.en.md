<p align="right" dir="ltr">
  <a href="./README.md" lang="fr" hreflang="fr" rel="alternate" title="Lire la doc en français" aria-label="Lire la doc en français">Français</a> · 🇬🇧 <strong>English</strong>
</p>

# Frontend Mentor – QR code component (solution)

[![Vite](https://img.shields.io/badge/Vite-⚡-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/) [![Tailwind CSS v4](https://img.shields.io/badge/Tailwind%20CSS-v4-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/) [![Netlify](https://img.shields.io/badge/Netlify-deploy-00C7B7?logo=netlify&logoColor=white)](https://www.netlify.com/) [![Live](https://img.shields.io/badge/Live-jb--fem--qr--code--component.netlify.app-brightgreen)](https://jb-fem-qr-code-component.netlify.app/)

This repo contains my solution to the **[QR code component](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H)** challenge by Frontend Mentor.

> 🎯 Personal objective: deliver an **accessible (a11y‑friendly), semantic, performant, and modern** component, with special attention to typography (locally hosted fonts, base size 1rem/16px for readability) and clean HTML structure. The tech choices (Vite + Tailwind v4) are intentional to refine my mastery of the stack.

---

## 🔎 Overview

### The challenge

- Display a **centered card** with a QR image and descriptive text.
- Follow the provided palette and type (Outfit 400/700).

### Screenshot

![Solution screenshot](https://jb-fem-qr-code-component.netlify.app/og.jpg)

### Links

- Live: [https://jb-fem-qr-code-component.netlify.app/](https://jb-fem-qr-code-component.netlify.app/)

---

## 🚀 Running the project

```bash
npm install
npm run dev      # local server
npm run build    # production build (dist/)
npm run preview  # preview the build
```

---

## 🧱 Built with

- **Semantic HTML5** (`main`, `article`, `img`)
- **Tailwind CSS v4** (`@theme` tokens: colors, fonts, radius)
- **Minimal Flex/Grid** (centering + `xs:` responsive)
- **Locally hosted WOFF2** fonts (Outfit 400/700)
- **Vite + Netlify** (preview)

---

## 🧭 Approach & implementation choices

### HTML structure

- **Tailwind v4 tokens**: `--color-slate-*`, `--color-accent`, `--radius-card`, `--spacing-card`, `--font-outfit` → utilities (`text-*`, `bg-*`, `rounded-*`, `p-card`, `font-outfit`).
- Footer links: readable underline + **focus ring**.

### Design System

- 16px base font size to improve readability.

### Fonts

- **Self‑hosted** in `public/fonts`, and **preload only** the critical weights (Outfit 700/400) to avoid _preloaded but not used quickly_ warnings; web audits.
- `font-synthesis-weight: none` to avoid fake bolding.

---

## ⚡ Performance

- **Tailwind v4 JIT** → minimal CSS.
- **WOFF2 fonts** + targeted `preload` + `swap`.

> Next step to explore: inline **critical CSS** via [`vite-plugin-beasties`](https://github.com/danielroe/beasties) to improve FCP/LCP.

---

## 🧪 My process

### Technologies used

- **Semantic HTML5 markup**
- **CSS custom properties** (via Tailwind v4 tokens in `@theme`)
- **Mobile‑first workflow**
- **Vite** (bundler/build)
- **Tailwind CSS v4**
- **Netlify** (hosting & headers)

### What I learned

- **v4 tokens** automatically generate utilities (e.g., `--color-accent` → `text-accent`, `bg-accent`).
- Preload resources used **above the fold** to avoid warnings.

### Continued development

- Export the QR PNG as WebP and try `<picture>`.

### Useful resources

- Tailwind v4 – `@theme` & tokens: [https://tailwindcss.com/docs/theme](https://tailwindcss.com/docs/theme)
- MDN – Responsive images (`<picture>`, `srcset`, `sizes`): [https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images](https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

---

## 👤 Author

- Website — [https://www.julienborgeon.fr](https://www.julienborgeon.fr)

---

## 🙌 Acknowledgments

Thanks to **Frontend Mentor** for the challenge design and to the community for feedback.
Shout‑out to MDN & Tailwind for their clear documentation.

---

## 📁 Project structure

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
