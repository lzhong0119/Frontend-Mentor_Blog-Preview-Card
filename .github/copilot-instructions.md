<!-- Copilot / AI agent guidance for the "Blog preview card" starter project -->
# Copilot instructions — Blog preview card

Purpose: help an AI coding agent work productively on this small static HTML/CSS project (Frontend Mentor starter).

Key points (quick):
- This is a single-page, no-build frontend challenge. The site is static HTML that expects a stylesheet at `styles.css` and local fonts in `assets/fonts/`.
- Design guidance and tokens live in `style-guide.md` (colors, font family, sizes). Use those values exactly when implementing styles.

Big picture
- The project is a simple responsive card built from `index.html` + `styles.css` (stylesheet is referenced but not included). The design assets are under `assets/` and a `design/` folder contains reference images for mobile/desktop.
- Primary goal: reproduce the visual design and required interaction states (hover + focus) while keeping HTML semantic and accessible.

Important files to reference
- `index.html` — page structure; includes a link to `styles.css` (create/modify this file).
- `style-guide.md` — canonical colors, typography, and breakpoint guidance (mobile 375px, desktop 1440px).
- `assets/fonts/` — local Figtree variable/static font files provided (use `@font-face` so the page works offline).
- `assets/images/` — illustrations, avatar, favicon used by the layout.
- `README-template.md` / `README.md` — repo instructions and submission guidance.

Project-specific patterns & conventions
- HTML-first: the starter expects the HTML skeleton to exist; add or change `styles.css` rather than embedding lots of new inline styles. Keep HTML semantic (article, header, footer, figure, figcaption where appropriate).
- Fonts: prefer local fonts from `assets/fonts/` (Figtree). Example approach:

```css
@font-face {font-family: 'Figtree'; src: url('./assets/fonts/Figtree-VariableFont_wght.ttf') format('truetype'); font-weight: 100 900;}
body { font-family: 'Figtree', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif; }
```

- Stylesheet path: `index.html` links to `styles.css` at the repo root — create that file if missing.
- Tokens: use the HSL values from `style-guide.md` (Yellow hsl(47, 88%, 63%), White hsl(0,0%,100%), Grays hsl(0,0%,42%) and hsl(0,0%,7%)).

Quick start / developer workflow (no build system)
- Open `index.html` directly in a browser for a quick check.
- Prefer running a local static server for correct font/media loading. Example (PowerShell):

```powershell
# from repo root
python -m http.server 8000
# then open http://localhost:8000
```

- Deploy: this challenge is normally published with GitHub Pages / Vercel / Netlify; no CI required.

Interaction and accessibility expectations
- Ensure hover and keyboard focus states are present for interactive items (links, buttons). The challenge explicitly requires visible hover+focus.
- Keep font-size for body around 16px (see `style-guide.md`). Test responsiveness across 320px–1440px.

Examples of actionable tasks for an AI agent
- If `styles.css` is missing: create `styles.css` and implement layout using the provided color tokens and font-face above, matching the mobile design first (375px), then add a media query for desktop (≥1024px or use the 1440px reference).
- If images are referenced but not used: ensure `assets/images/illustration-article.svg` and `assets/images/image-avatar.webp` are placed in `figure`/`img` with appropriate `alt` text.

What not to do
- Don't add build tooling (webpack, gulp) or frameworks — this repository expects a simple static solution.
- Avoid changing the provided `design/` images; use them only as visual references.

If you need more context
- Read `style-guide.md` and `README-template.md` for scoring/submission rules.

When done, leave a concise PR description that mentions which files changed (typically `styles.css` and small HTML adjustments) and confirm that hover+focus states and local font loading were implemented.

If anything here is unclear or you want more examples (CSS snippets for the card layout, suggested breakpoints, or accessibility checklist), tell me which section to expand.
