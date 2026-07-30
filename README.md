# Chrome Credits Open Source Viewer

**Build trust. Showcase transparency. Power your website development with professional open-source attribution.**

This project delivers a modern, interactive recreation of Chrome's `chrome://credits/` page — the complete open-source software licenses used in Chromium-based browsers. Perfect for business websites, SaaS products, marketing compliance pages, developer portfolios, and legal transparency hubs.

## Why This Matters for Your Business & Marketing

- **Legal Compliance**: Properly attribute third-party open-source components (required by BSD, Apache, MIT, LGPL licenses).
- **Brand Trust**: Display professional credits to build credibility with customers and partners.
- **Website Development Ready**: Clean JavaScript, responsive design, ready for GitHub Pages or any static host.
- **Marketing Asset**: Use as a "Transparency" or "Open Source" page to differentiate your brand.

## Live Demo (Enable GitHub Pages)

1. Go to repository **Settings → Pages**.
2. Source: Deploy from branch `main` / root.
3. Your site will be live at: `https://pointgoddesscc-sketch.github.io/chrome-credits-open-source/`

## Features

- Interactive expand/collapse license texts (exactly like Chrome)
- Search & filter components
- Print-friendly
- Dark/light mode ready
- Fully documented JavaScript
- Sample of major Chromium licenses + structure to add the full set

## Quick Start (Website Development)

```bash
git clone https://github.com/pointgoddesscc-sketch/chrome-credits-open-source.git
cd chrome-credits-open-source
# Open index.html in browser or serve with any static server
npx serve .
```

## JavaScript Documentation

See **[docs/JS_DOCUMENTATION.md](docs/JS_DOCUMENTATION.md)** for complete API, functions, and best practices for extending this credits viewer in your own website projects.

## Full License Coverage

`chrome://credits/` contains **hundreds** of third-party components.  
This repository includes:

- Core Chromium (BSD-3-Clause)
- V8 JavaScript Engine (BSD)
- Blink / WebKit (BSD + LGPL)
- Angle, Skia, and other key libraries
- Structure and instructions to import the complete set from official Chromium source or [TeamDev Chromium-Licences](https://github.com/TeamDev-IP/Chromium-Licences)

To generate the absolute latest full credits:

```bash
# From a Chromium source checkout
python3 tools/licenses/licenses.py credits > full_credits.html
```

## Project Structure

```
├── index.html              # Main interactive credits page (JS + CSS)
├── licenses/               # Individual license text files
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
