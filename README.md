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

### 🪄 Quick Start

```jsx
import React from "react";
import {
  Button,
  Input,
  Select,
  Checkbox,
  Switch,
  Card,
  Modal,
  Tooltip,
} from "@tuanlee-tech/tsm-ui";

import "@tuanlee-tech/tsm-ui/dist/index.css"; // Optional global styles

export default function App() {
  return (
    <div style={{ padding: 24 }}>
      <h2>Welcome to TSM-UI ✨</h2>

      <Input placeholder="Enter your name" />

      <Button variant="primary" style={{ marginTop: 12 }}>
        Submit
      </Button>

      <Checkbox label="Accept terms" />
      <Switch checked />

      <Card title="Example Card">
        <p>This is a card component.</p>
      </Card>

      <Tooltip text="Hello from TSM-UI!">
        <span style={{ cursor: "pointer", textDecoration: "underline" }}>
          Hover me
        </span>
      </Tooltip>
    </div>
  );
}
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

TSM-UI uses a unified theme system powered by **JavaScript theme object** and **CSS variables**.

You can customize the look of all components in two main ways:

#### 1️⃣ **Edit `theme.js`**

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

If your app imports the library source or you fork the repo,
you can edit `theme.js` directly and rebuild.

---

#### 2️⃣ **Override CSS Variables**

All theme tokens are automatically mapped to CSS variables.
Simply redefine them in your global CSS:

```css
:root {
  --color-primary: #ff4d6d;
  --color-background: #ffffff;
  --color-text: #111111;
  --color-border: #e5e7eb;
}

body {
  background-color: var(--color-background);
  color: var(--color-text);
}
```

This allows **dynamic theming** (e.g., dark/light mode) without changing the build.

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
