# Chrome Credits Open Source Viewer

**Build trust. Showcase transparency. Power your website development with professional open-source attribution.**

This project delivers a modern, interactive recreation of Chrome's `chrome://credits/` page — the complete open-source software licenses used in Chromium-based browsers. Perfect for business websites, SaaS products, marketing compliance pages, developer portfolios, and legal transparency hubs.

## Live Demo (Working Right Now)

**Production URL (Vercel):**  
https://chrome-credits-open-source-pse-sent.vercel.app

Also available at:  
https://chrome-credits-open-source-pointgoddesscc-8694-pse-sent.vercel.app

## Why You Saw 404 on GitHub Pages

GitHub Pages is **not automatically enabled**. You must turn it on once:

1. Go to the repository: https://github.com/pointgoddesscc-sketch/chrome-credits-open-source
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main`  /  Folder: `/ (root)`
5. Click **Save**

After 1–2 minutes the site will be live at:  
`https://pointgoddesscc-sketch.github.io/chrome-credits-open-source/`

## Local Working Copy – Port 400

Perfect for development and testing on your machine:

```bash
git clone https://github.com/pointgoddesscc-sketch/chrome-credits-open-source.git
cd chrome-credits-open-source
npm install          # optional – installs serve
npm start            # or npm run dev
```

Open: **http://localhost:400**

Alternative (no npm install needed):
```bash
npx serve . -p 400
```

## Features

- Interactive expand/collapse license texts (exactly like Chrome)
- Search & filter components
- Print-friendly
- Dark/light mode ready
- Fully documented JavaScript
- Sample of major Chromium licenses + structure to add the full set

## JavaScript Documentation

See **[docs/JS_DOCUMENTATION.md](docs/JS_DOCUMENTATION.md)** for complete API, functions, and best practices for extending this credits viewer in your own website projects.

## Full License Coverage

`chrome://credits/` contains **hundreds** of third-party components.  
This repository includes:

- Core Chromium (BSD-3-Clause)
- V8 JavaScript Engine (BSD)
- Blink / WebKit (BSD + LGPL)
- ANGLE and other key libraries
- Structure and instructions to import the complete set from official Chromium source or community mirrors

## Project Structure

```
├── index.html              # Main interactive credits page (JS + CSS)
├── package.json            # Local server scripts (port 400)
├── docs/
│   └── JS_DOCUMENTATION.md # Full JavaScript developer docs
├── LICENSE                 # MIT license for this project
└── README.md
```

## Marketing & Business Use Cases

- Add `/credits` or `/open-source` page to your SaaS / product site
- Compliance for commercial products embedding Chromium (Electron, CEF, etc.)
- Portfolio piece demonstrating clean modern JavaScript website development
- Educational resource for open-source licensing

## Contributing

Pull requests welcome for additional license entries, improved JS interactivity, or internationalization.

---

**Built for website developers, marketers, and businesses who value transparency.**  
Powered by clean, documented JavaScript.
