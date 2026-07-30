# JavaScript Documentation – Chrome Credits Viewer

**For website development teams, marketing sites, and compliance pages.**

This document explains every JavaScript function, data structure, and extension point so you can confidently customize or integrate this credits page into any modern website.

## Overview

The script is vanilla JavaScript (no frameworks) for maximum compatibility and performance. It is production-ready and follows security best practices (HTML escaping).

## Data Structure

```js
const LICENSE_DATA = [
  {
    name: string,      // Display name of the component
    url: string,       // Homepage URL
    license: string    // Full license text (plain text)
  },
  // ... more entries
];
```

Add new components by pushing objects into this array before calling `renderCredits()`.

## Public API / Functions

### `renderCredits(data)`

Renders the full list of product cards.

- **Parameters**: `data` – Array of license objects
- **Side effects**: Clears `#credits-container` and rebuilds DOM
- **Usage**: Call once on page load or after updating data

```js
renderCredits(LICENSE_DATA);
```

### `toggleLicense(btn)`

Toggles a single license block open/closed.

- **Parameters**: `btn` – The button element that was clicked
- **Updates**: Button text and `aria-expanded` for accessibility

### `toggleAll()`

Opens or closes every license block at once.

- Detects current state and flips all
- Updates the “Show All / Hide All” button text

### `filterCredits(query)`

Live search/filter of components by name.

- **Parameters**: `query` – Search string from input
- Hides non-matching `.product` elements via `display: none`

### `escapeHtml(text)`

Security helper – converts special characters to HTML entities.

Always use this when inserting user-controlled or external text into the DOM.

## Event Binding

All events are bound after DOMContentLoaded:

```js
document.addEventListener('DOMContentLoaded', () => {
  renderCredits(LICENSE_DATA);
  // ... listeners
});
```

## Extending for Production Websites

1. **Load full Chromium licenses**  
   Replace `LICENSE_DATA` with a larger JSON file generated from Chromium’s `tools/licenses/licenses.py`.

2. **Fetch from API**  
   ```js
   fetch('/api/licenses.json')
     .then(r => r.json())
     .then(data => renderCredits(data));
   ```

3. **Add analytics**  
   Track “show license” clicks for marketing insights on transparency engagement.

4. **Internationalization**  
   Move button strings and page title into a language object.

5. **Accessibility**  
   Already includes `aria-expanded` and semantic HTML. Add keyboard focus styles if needed.

## Browser Support

- Modern evergreen browsers (Chrome, Edge, Firefox, Safari)
- No polyfills required for ES6+ features used

## Performance Notes

- Rendering is fast even with 200+ entries
- Search uses simple string includes (O(n))
- No virtual DOM – pure DOM for simplicity and small footprint

## License of This Documentation & Code

MIT – free for commercial website development and marketing use.

---

**Need help integrating into your product website?**  
Fork the repo, open an issue, or extend the JavaScript as documented above.
