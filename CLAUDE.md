# Portfolio website

Hugo site for a personal research portfolio, deployed to GitHub Pages. See README.md for usage (including Hugo 0.166 template notes).

## Rules that keep it what it is
- **Lightweight is the top priority.** No npm, no CSS framework. The only build tool is the `hugo` binary. A Hugo theme is allowed. Small inline JavaScript is allowed when it earns its place; no JS libraries. Ask before adding any other dependency.
- **Content is markdown, layout is templates.** Do not hardcode prose or data in templates. Adding a project must only need one new file in `content/projects/`, a role one file in `content/experience/`; home page groups come from `data/groups.toml`. Keep templates small and single-purpose (one partial per component); links go through `_partials/func/resolve-url.html`.
- **Stylesheets** live in `assets/css/`, one file per concern, bundled in the order listed in `_partials/site/head.html`. Every color, size and space is a token in `tokens.css`; components use tokens only. Fonts are self-hosted from `static/fonts/`. The theme follows the visitor's OS/browser preference (`prefers-color-scheme`). Dark backgrounds stay near-neutral; fern green (`--accent`) is the only color.
- Content stays honest: unverified facts are written as `TODO`, not invented.
