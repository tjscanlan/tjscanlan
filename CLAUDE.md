# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

This is TJ Scanlan's GitHub profile repository (`tjscanlan/tjscanlan`), rendered as both:
- The special `README.md` shown on his GitHub profile page.
- A single-page static site (`index.html`) served via GitHub Pages, styled as a fake terminal/eval-run theme ("run-eval --suite=tj-scanlan").

There is no application code, no package manager, and no test suite — this repo is content, not software.

## Structure

- `README.md` — GitHub profile README content (bio, tech stack, pinned projects).
- `index.html` — the standalone Pages site. All CSS and JS live inline in this one file (no build step, no external JS bundle). The JS handles: a typewriter effect for the terminal block, an `IntersectionObserver` for active-section highlighting in the sidebar nav, and a `prefers-reduced-motion` fallback that renders content statically.
- `.github/workflows/static.yml` — deploys the repo root straight to GitHub Pages via `actions/upload-pages-artifact` + `actions/deploy-pages` on every push to `main` (or manual dispatch). No Jekyll involved — `index.html` is served as-is. The repo's Pages source must be set to "GitHub Actions" (Settings → Pages) for this to take effect.

## Working in this repo

- `README.md` and `index.html` intentionally duplicate the same bio/project content in two different formats/tones (Markdown for GitHub profile, terminal-themed HTML for Pages). When updating bio, job history, tech stack, or pinned projects, update both files unless the change is presentation-only.
- `index.html` has no separate CSS/JS files — keep edits inline within the existing `<style>`/`<script>` blocks rather than splitting them out, unless asked to restructure the site.
- To preview `index.html` locally, just open it directly in a browser (`open index.html` on macOS) — no server or build step is required.
