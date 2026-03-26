# CLAUDE.md — Joe Manbeck Portfolio Website

## Always Do First
- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.
- **Invoke the `web-design-guidelines` skill** alongside `frontend-design` for every new page or major component.

## Project Context
- Personal portfolio/resume site for **Joe Manbeck**, Product Leader
- Vibe: sophisticated, dark, professional — product-tech focused
- Single-page site: Hero, Work/Experience, Highlights/Projects, Skills, Volunteer, Contact

## Design System
- **Background:** `#0B0C0A` (near-black warm)
- **Surface:** `#131510` / `#1A1E16` / `#22271D` (layered dark surfaces)
- **Text:** `#E8EBE2` (warm off-white) / `#7A8070` (muted)
- **Accent:** `#4FD87A` (vivid green)
- **Fonts:** Cormorant (display/headings) + DM Sans (body) — both via Google Fonts

## Local Server
- **Always serve on localhost** — never screenshot a `file:///` URL.
- Start: `node serve.mjs` (serves project root at `http://localhost:3000`)
- If port 3000 is in use, kill it first: `npx kill-port 3000`

## Screenshot Workflow
- Puppeteer is at `C:/Users/dflet/AppData/Local/Temp/puppeteer-test/`
- Run screenshot from the **TomNJerrys** project directory (puppeteer is installed there):
  `cd ../TomNJerrys && node screenshot.mjs http://localhost:3000 label`
- Screenshots saved to `./temporary screenshots/` (in TomNJerrys project)
- After screenshotting, read the PNG with the Read tool to visually inspect

## Output Defaults
- Single `index.html` file, all styles inline
- Tailwind CSS via CDN
- Placeholder images: `https://placehold.co/WIDTHxHEIGHT`
- Mobile-first responsive

## Hard Rules
- Do not use light/pastel color schemes — dark only
- Do not use `transition-all`
- Do not use default Tailwind blue/indigo as primary color
- Every clickable element needs hover, focus-visible, and active states
- Only animate `transform` and `opacity`
