# Project Overview

This is a static, single-page web application acting as a landing page for "TATVAM 2026 — Riwaayat," a college cultural festival. The primary feature of the page is a live countdown timer targeting June 4, 2026 (IST).

**Main Technologies:**
- Vanilla HTML5
- Vanilla CSS3 (Embedded)
- Vanilla JavaScript (Embedded)
- No external frameworks, libraries, or build tools are used.

**Architecture:**
The entire application is contained within a single `index.html` file.
- **Styling:** CSS is embedded in the `<head>` and makes extensive use of CSS variables (Custom Properties) for design tokens (colors, typography, spacing). It features custom base64-encoded fonts and responsive design using `clamp()`. It also includes accessibility features like `prefers-reduced-motion` support.
- **Logic:** JavaScript is embedded at the end of the `<body>` to handle the countdown timer logic, updating the DOM elements every second until the target date is reached.
- **Assets:** Decorative elements (corners, dividers, ornaments) are implemented as inline SVGs.

# Building and Running

Since this is a simple static HTML file without any build steps or dependencies, it can be run instantly.

**To run the project locally:**
1. Simply open the `index.html` file directly in any modern web browser.
2. Alternatively, for a more accurate representation of how it might behave when hosted, use any basic local web server from the project directory. For example:
   - Using Python 3: `python -m http.server`
   - Using Node.js: `npx serve` or `npx http-server`

**To build/deploy:**
No build step is required. The `index.html` file is ready to be deployed directly to any static file hosting service (e.g., GitHub Pages, Netlify, Vercel, or a standard web server).

# Development Conventions

Based on the existing codebase, adhere to the following conventions when making modifications:

- **Zero Dependencies:** Maintain the vanilla approach. Do not introduce external libraries (like jQuery, moment.js), frameworks (like React, Vue, TailwindCSS), or build steps unless explicitly required and approved.
- **Single File Structure:** Keep all HTML, CSS, and JS within `index.html` to maintain the current architecture, unless the file grows significantly and modularization is requested.
- **CSS Design Tokens:** When tweaking visuals (colors, fonts, spacing), update the existing CSS variables in the `:root` selector rather than hardcoding values in specific CSS rules.
- **Responsive Design:** Continue using modern CSS features like `clamp()` for fluid typography and sizing to ensure smooth scaling across devices.
- **Inline SVGs:** Use inline SVGs for vector graphics to avoid additional HTTP requests and to allow easy styling via CSS (e.g., `stroke` and `fill`).
- **Accessibility:** Maintain the established accessibility standards. Use semantic HTML, `aria-*` attributes (like `aria-live` for the timer), and respect `prefers-reduced-motion` media queries.
- **JavaScript Simplicity:** Keep the logic straightforward. The current script uses native DOM APIs and `setInterval`. Maintain clear comments and avoid over-engineering.