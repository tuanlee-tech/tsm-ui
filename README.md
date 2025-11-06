# 🧩 @tuanlee-tech/tsm-ui

[![npm version](https://img.shields.io/npm/v/@tuanlee-tech/tsm-ui.svg?color=00D9FF)](https://www.npmjs.com/package/@tuanlee-tech/tsm-ui)
[![npm downloads](https://img.shields.io/npm/dm/@tuanlee-tech/tsm-ui.svg?color=00D9FF)](https://www.npmjs.com/package/@tuanlee-tech/tsm-ui)
[![license](https://img.shields.io/npm/l/@tuanlee-tech/tsm-ui.svg)](./LICENSE)
[![bundle size](https://img.shields.io/bundlephobia/minzip/@tuanlee-tech/tsm-ui?color=00D9FF)](https://bundlephobia.com/package/@tuanlee-tech/tsm-ui)

**@tuanlee-tech/tsm-ui** is a lightweight React UI component library built for modern apps —
beautiful, minimal, and fully customizable with your own theme.

---

### 🚀 Features

- ⚡ **Lightweight & Tree-shakable** — built with Rollup for optimal performance
- 🎨 **Customizable Theme System** — easily change colors, spacings, borders, etc.
- 💅 **Scoped CSS with CSS Variables** — simple global styling via `global.css`
- 🧱 **Composable Components** — flexible and reusable
- 🧰 **Framework Compatible** — works perfectly with **Vite**, **CRA**, **Next.js**, and more

---

### 📦 Installation

```bash
npm install @tuanlee-tech/tsm-ui
# or
yarn add @tuanlee-tech/tsm-ui
# or
pnpm add @tuanlee-tech/tsm-ui
```

---

### 🧩 Components List

| Component    | Description                                                         |
| ------------ | ------------------------------------------------------------------- |
| **Button**   | Reusable button with multiple variants (`primary`, `outline`, etc.) |
| **Input**    | Simple and accessible input field                                   |
| **Select**   | Dropdown select with styling                                        |
| **Checkbox** | Styled checkbox component                                           |
| **Switch**   | Toggle switch for boolean states                                    |
| **Card**     | Wrapper with shadow and padding                                     |
| **Modal**    | Overlay dialog with content                                         |
| **Tooltip**  | Hover-based tooltip with animation                                  |

---

### 🎨 Theming & Custom Styles

TSM-UI uses a unified theme system powered by **JavaScript theme objects** and **CSS variables**.

You can customize the look of all components in two ways:

---

#### 1️⃣ **Edit `theme.js` (for forked or local builds)**

```js
// ==================== src/ui/theme.js ====================

export const theme = {
  colors: {
    primary: "#00D9FF",
    background: "#0a0e1a",
    text: "#e4e4e7",
    // ...other tokens
  },
  spacing: {
    sm: "8px",
    md: "12px",
    lg: "16px",
  },
  borderRadius: {
    md: "8px",
    lg: "12px",
  },
  shadows: {
    sm: "0 2px 8px rgba(0, 0, 0, 0.2)",
  },
};
```

If you fork the repo or use the source directly, you can edit `theme.js` and rebuild.

---

#### 2️⃣ **Override CSS Variables (Recommended)**

All theme tokens are mapped to CSS variables automatically.
You can redefine them anywhere in your app — the most flexible and common approach.

##### ✅ Example: `src/theme.css`

```css
/* ==================== src/theme.css ==================== */
/* Override default colors of TSM-UI */

:root {
  --color-primary: #6366f1;
  --color-primary-dark: #4f46e5;
  --color-background: #0b1120;
  --color-background-light: #1e1b4b;
  --color-background-lighter: #312e81;
  --color-border: #4338ca;
  --color-border-light: #6366f1;
  --color-text: #f1f5f9;
  --color-text-secondary: #c7d2fe;
  --color-text-muted: #a5b4fc;
  --color-error: #f43f5e;
  --color-success: #10b981;
  --color-warning: #fbbf24;
}

body {
  background: var(--color-background);
  color: var(--color-text);
  transition: background 0.3s ease, color 0.3s ease;
}
```

##### ✅ Import in your entry file (e.g. `main.jsx`)

```jsx
import "@tuanlee-tech/tsm-ui/dist/index.css"; // Base library styles
import "./theme.css"; // ✅ Custom overrides (must come AFTER)
```

> 🧠 **Tip:** Always import your custom theme file _after_ the library CSS to ensure your colors take effect.

---

#### 🌗 Optional: Dynamic Dark/Light Mode

You can define multiple themes and switch between them dynamically.

```css
:root[data-theme="dark"] {
  --color-background: #0b1120;
  --color-primary: #6366f1;
}

:root[data-theme="light"] {
  --color-background: #ffffff;
  --color-primary: #2563eb;
  --color-text: #111827;
}
```

Then toggle via JavaScript:

```js
document.documentElement.setAttribute("data-theme", "dark");
```

---

### 🏗️ Folder Structure

```
tsm-ui/
├── src/
│   ├── components/
│   │   ├── Button/
│   │   ├── Input/
│   │   ├── Select/
│   │   ├── Checkbox/
│   │   ├── Switch/
│   │   ├── Card/
│   │   ├── Modal/
│   │   └── Tooltip/
│   ├── ui/
│   │   ├── theme.js
│   │   └── global.css
│   └── index.js          # Export all components
├── dist/                 # Build output
├── rollup.config.js
├── package.json
└── README.md
```

---

### ⚙️ Development & Build

#### Install dependencies

```bash
npm install
```

#### Build the library

```bash
npm run build
```

#### Watch mode (auto rebuild on save)

```bash
npm run watch
```

---

### 🧾 License

**MIT © 2025** — Built with ❤️ by [Tuan Lee](https://github.com/tuanlee-tech)

---

### 🌐 Links

- **NPM:** [@tuanlee-tech/tsm-ui](https://www.npmjs.com/package/@tuanlee-tech/tsm-ui)
- **GitHub:** [github.com/tuanlee-tech/tsm-ui](https://github.com/tuanlee-tech/tsm-ui)

---
