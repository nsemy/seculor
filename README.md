# Seculor — Cybersecurity Consulting Website

Official website for **Seculor**, a cybersecurity consulting firm based in Québec. The site presents services, methodology, and contact information in both **French and English**.

🌐 [seculor.ca](https://seculor.ca)

---

## About

Seculor helps organizations build a solid cybersecurity posture through three core services: incident response planning, vulnerability management, and security governance. This website serves as the firm's public-facing presence and lead generation point.

---

## Features

- **Bilingual (FR / EN)** — full language toggle in the navbar, switching all page content instantly
- **Single-file HTML** — no build tools, no dependencies, no frameworks
- **Embedded Google Form** — contact form with language-aware iframes (FR + EN)
- **Fully responsive** — mobile-friendly layout
- **Pure CSS animations** — blinking badge, hover effects, smooth scroll
- **Google Fonts** — Cormorant Garamond + DM Sans

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (custom properties, grid, flexbox) |
| Interactivity | Vanilla JavaScript (no libraries) |
| Fonts | Google Fonts |
| Contact Form | Google Forms (embedded iframe) |
| Hosting | *(your hosting provider here)* |

---

## File Structure

```
/
├── index.html        # Main website (bilingual)
└── README.md         # This file
```

---

## Bilingual System

Language switching is handled entirely in JavaScript without any external i18n library. All translatable strings are stored in a `translations` object at the bottom of `index.html`:

```javascript
const translations = {
  fr: { "hero.h1": "Préparez-vous avant qu'un incident ne survienne", ... },
  en: { "hero.h1": "Be ready before an incident strikes", ... }
};
```

HTML elements use `data-i18n` (plain text) or `data-i18n-html` (HTML with tags like `<em>`) attributes to bind to translation keys:

```html
<h1 data-i18n-html="hero.h1">...</h1>
```

Calling `setLang('en')` or `setLang('fr')` updates all bound elements and swaps the Google Form iframe.

---

## Google Form — Adding a Full English Version

Currently, the English form uses `?hl=en` which translates Google's UI (Submit button, validation messages). To also translate the **question labels**:

1. Open your form in [Google Forms](https://forms.google.com)
2. Click the three-dot menu → **Make a copy**
3. Translate all question labels to English
4. Click **Send** → get the embed link
5. In `index.html`, replace the `src` of `#form-en` with the new English form URL

---

## Local Development

No build step required. Just open the file in a browser:

```bash
# Option 1 — open directly
open index.html

# Option 2 — serve locally (recommended to avoid iframe restrictions)
npx serve .
# or
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

---

## Deployment

The site is a single static HTML file and can be deployed to any static host:

- **cPanel / FTP** — upload `index.html` to your `public_html` folder
- **GitHub Pages** — push to `main` branch and enable Pages in repository settings
- **Netlify / Vercel** — connect this repository and deploy automatically

---

## Contact

**Seculor**
📧 info@seculor.ca
📞 514-951-7642

---

© 2025 Seculor. All rights reserved.
