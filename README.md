# Next.js + Tailwind CSS Project Structure (JavaScript)

This repository contains a modular, production-ready **Next.js App Router** project folder structure built with **pure JavaScript** (`.js` / `.jsx`) and **Tailwind CSS** integrated into the root layout and primary layout across all pages.

---

## 📁 Project Folder Structure

```text
note/
├── app/
│   ├── about/
│   │   └── page.js          # About route (/about)
│   ├── contact/
│   │   └── page.js          # Interactive Contact route (/contact)
│   ├── services/
│   │   └── page.js          # Services & capabilities route (/services)
│   ├── globals.css          # Global stylesheet with Tailwind directives & tokens
│   ├── layout.js            # Root Layout wrapping all pages with PrimaryLayout
│   └── page.js              # Home landing page (/)
│
├── components/
│   ├── layout/
│   │   ├── Navbar.js        # Responsive top navigation bar with brand identity
│   │   ├── Footer.js        # Site-wide responsive footer with links & status
│   │   └── PrimaryLayout.js # Unified primary shell providing layout to all pages
│   └── ui/
│       ├── Button.js        # Reusable Tailwind button component with variants
│       └── Card.js          # Reusable glassmorphic Tailwind card component
│
├── lib/
│   └── utils.js             # Utility functions (cn class combiner)
│
├── public/                  # Static assets (images, icons, fonts)
├── .gitignore               # Standard Next.js git ignore configuration
├── jsconfig.json            # Path alias configuration (@/* mapping)
├── next.config.mjs          # Next.js configuration
├── package.json             # Project dependencies and dev scripts
├── postcss.config.mjs       # PostCSS plugins for Tailwind CSS & Autoprefixer
├── tailwind.config.js       # Tailwind CSS theme extension & content scanner
└── README.md                # Project architecture documentation
```

---

## 🚀 Key Architectural Highlights

1. **Root Layout (`app/layout.js`)**:
   - Imports `globals.css` with Tailwind CSS directives (`@tailwind base`, `@tailwind components`, `@tailwind utilities`).
   - Configures global document metadata (SEO tags, titles, descriptions, viewport).
   - Injects the `PrimaryLayout` shell component directly around `{children}`.

2. **Primary Layout (`components/layout/PrimaryLayout.js`)**:
   - Houses the sticky glassmorphic `Navbar` and the responsive `Footer`.
   - Adds background ambient lighting and consistent container constraints (`max-w-7xl mx-auto`).
   - Automatically wraps **all pages** without needing manual imports on each sub-route.

3. **Pure JavaScript**:
   - Uses `.js` and standard React JSX syntax without requiring TypeScript build steps.
   - `jsconfig.json` provides `@/*` path aliases for clean imports.

4. **Tailwind CSS Ready**:
   - Configured with `tailwind.config.js` and `postcss.config.mjs`.
   - Content array set to scan `app/**/*.{js,jsx}` and `components/**/*.{js,jsx}`.

---

## 🛠️ Quick Start

Install dependencies and start the local development server:

```bash
# 1. Install dependencies
npm install

# 2. Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.
