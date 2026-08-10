# mmy-css ⚡

A modern, ultra-lightweight CSS framework under **1.2 KB gzipped**.

[![NPM Version](https://img.shields.io/npm/v/mmy-css?color=2563eb&style=flat-square)](https://www.npmjs.com/package/mmy-css)
[![Bundle Size](https://img.shields.io/badge/bundle%20size-1.2%20KB%20gzipped-10b981?style=flat-square)](https://www.npmjs.com/package/mmy-css)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/mmy-lana/mmy-css?style=flat-square)](https://github.com/mmy-lana/mmy-css)

---

## 🌟 Why mmy-css?

Most CSS frameworks ship dozens of kilobytes of unneeded rules. **mmy-css** gives you a responsive layout, modern typography, forms, buttons, cards, tables, and auto dark mode—all in a package smaller than a single icon.

- 📦 **Micro Bundle:** Under 1.2 KB gzipped (~3.1 KB uncompressed).
- 🚀 **Zero Dependencies & Zero JS:** Pure CSS built on modern web standards.
- 🎨 **Themeable:** Powered by CSS custom properties (`:root` variables).
- 🌙 **Automatic Dark Mode:** Out-of-the-box support for `prefers-color-scheme: dark`.
- 📐 **Zero-Specificity Resets:** Uses `:where()` selectors so you can override styles effortlessly without `!important`.
- 🔤 **Fluid Typography:** Uses CSS `clamp()` for responsive text scaling across all viewports.

---

## 🚀 Quick Start

### Option 1: Install via NPM

```bash
npm install mmy-css
```

Import it in your main JavaScript / TypeScript entry point (React, Vue, Svelte, Next.js, Vite, etc.):

```javascript
import 'mmy-css';
```

### Option 2: Use via CDN (No Build Step)

Drop this single line into the `<head>` of your HTML file:

```html
<!-- unpkg CDN -->
<link rel="stylesheet" href="https://unpkg.com/mmy-css/dist/mmy.min.css">

<!-- jsDelivr CDN -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/mmy-css/dist/mmy.min.css">
```

---

## 🎨 Design System & Customization

`mmy-css` uses CSS custom properties for instant re-theming. Override any token in your own stylesheet:

```css
:root {
  --primary: #8b5cf6;        /* Change primary brand color */
  --primary-hover: #7c3aed;  /* Change button hover color */
  --radius: 0.75rem;         /* Make all cards/buttons extra rounded */
  --font-sans: 'Inter', system-ui, sans-serif;
}
```

### Available Tokens

| Token | Default (Light) | Default (Dark) | Description |
| :--- | :--- | :--- | :--- |
| `--bg` | `#ffffff` | `#0f172a` | Main page background |
| `--surface` | `#f9fafb` | `#1e293b` | Card & table background |
| `--text` | `#111827` | `#f8fafc` | Primary text color |
| `--text-muted` | `#6b7280` | `#94a3b8` | Secondary / caption text |
| `--border` | `#e5e7eb` | `#334155` | Hairline border color |
| `--primary` | `#2563eb` | `#3b82f6` | Brand / action color |
| `--radius` | `0.375rem` | `0.375rem` | Corner rounding radius |

---

## 📖 Component Examples

### 1. Buttons & Badges

```html
<!-- Primary Button -->
<button class="btn">Click Me</button>

<!-- Outline Button -->
<button class="btn btn-outline">Outline</button>

<!-- Link styled as a Button -->
<a href="#" class="btn">Link Button</a>

<!-- Pill Badge -->
<span class="badge">New Release</span>
```

### 2. Form Controls

```html
<input type="text" class="input" placeholder="Your name...">

<select class="select">
  <option>Option 1</option>
  <option>Option 2</option>
</select>

<textarea class="textarea" placeholder="Message..."></textarea>
```

### 3. Cards & Auto-Fit Grid

No media queries required! The grid automatically adjusts column counts based on container width.

```html
<div class="grid">
  <div class="card">
    <h3>Card Title 1</h3>
    <p class="text-muted">Auto responsive column.</p>
  </div>
  <div class="card">
    <h3>Card Title 2</h3>
    <p class="text-muted">Auto responsive column.</p>
  </div>
</div>
```

### 4. Flex Utilities

```html
<div class="flex items-center justify-between">
  <h2>Dashboard</h2>
  <button class="btn">Add New</button>
</div>
```

---

## 🌙 Dark Mode

Dark mode is **100% automatic** based on the user's system preferences (`prefers-color-scheme`).

If you want to allow users to manually toggle dark/light mode with a button, set the `color-scheme` property on `<html>` using JavaScript:

```javascript
// Toggle between light and dark mode
const isDark = document.documentElement.style.getPropertyValue('color-scheme') === 'dark';
document.documentElement.style.setProperty('color-scheme', isDark ? 'light' : 'dark');
```

---

## 🛠️ Local Development

If you want to contribute or build `mmy-css` locally:

```bash
# 1. Clone repository
git clone https://github.com/mmy-lana/mmy-css.git
cd mmy-css

# 2. Install dev dependencies
npm install

# 3. Start dev server & watch mode
npm run dev

# 4. Build minified bundle & check gzipped size
npm run build
```

---

## 📄 License

Distributed under the [MIT License](LICENSE). Created by **Muhammad maulana Yusuf** ([@mmy-lana](https://github.com/mmy-lana)).
