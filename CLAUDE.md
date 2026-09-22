# Portfolio website

Hugo site for a personal research portfolio, deployed to GitHub Pages. See README.md for usage.

## Rules that keep it what it is
- **Lightweight is the top priority.** No JavaScript, no npm, no theme, no CSS framework. The only tool is the `hugo` binary. Ask before adding any dependency.
- **Content is markdown, layout is templates.** The home page (`content/_index.md`) and project pages (`content/projects/*.md`) go through the same `layouts/baseof.html` and the same `.prose` styles. Do not hardcode prose or data in templates. Adding a project must only need one new `.md` file.
- **One stylesheet** (`assets/css/style.css`). Colors are tokens at the top. **Light is the default for every visitor**, not tied to OS/browser preference; dark mode is opt-in via `[data-theme="dark"]` on `<html>` (nothing sets that yet). Dark backgrounds stay near-neutral, green is only the accent.
- **Handwritten font (`.hand`, Caveat) is for short annotations only**: blockquote margin notes, image captions, project status, footer sign-off. Never headings, nav, labels or body text.
- Content stays honest: unverified facts are written as `TODO`, not invented.

## Hugo 0.166 notes
- New layout folder names: `_partials/`, `_shortcodes/`, `_markup/`, `home.html`, `projects/page.html`.
- `relURL` leaves `/path` untouched (only `/` and fragments get the base path). Strip the leading slash first, or use `site.Home.RelPermalink`.
- `hugo.toml` has `baseURL = "/"` for local preview; CI passes the real one.
