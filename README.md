# Portfolio website

A small, static research portfolio built with [Hugo](https://gohugo.io) and hosted on GitHub Pages. No theme, no JavaScript, no dependencies beyond the `hugo` binary. Every page is a markdown file.

## Run locally

Install Hugo (standard edition, v0.166 or newer), then:

```sh
hugo server        # live preview at http://localhost:1313
hugo server -D     # also show drafts
```

## Edit content

| To change | Edit |
|---|---|
| Home page (bio, research list, section text) | `content/_index.md` |
| Name, footer links, nav, site description | `hugo.toml` |
| A project page | `content/projects/<slug>.md` |

**Add a project**

```sh
hugo new projects/my-project.md
```

Fill in the front matter (`title`, `summary`, `tags`, optional `status` and `links`), write the page in markdown, and delete `draft: true`. The card on the home page appears automatically, newest `date` first (undated pages go last). Drafts are hidden from the build, and so are pages with a future `date`.

**Markdown features**

- Standard markdown: headings, lists, links, tables, footnotes, code blocks (plain, no highlighting).
- `> a blockquote` renders as a handwritten margin note. Keep them short.
- `![alt](path "caption")` renders an image with a handwritten caption. `path` can be a file next to the page (use a folder `content/projects/<slug>/index.md` and put images beside it) or a file under `static/`, written with a leading slash, e.g. `/img/photo.jpg`.
- `{{< gallery >}} ...images... {{< /gallery >}}` lays images out in a grid.
- `{{< projects >}}` inserts the project card grid.
- Raw HTML is disabled. For links to other pages of this site, use `{{< relref "projects/slug" >}}` so they keep working under the GitHub Pages sub-path.

## Deploy

Pushing to `main` runs `.github/workflows/hugo.yml`, which builds the site and publishes it. One-time setup: in the GitHub repo, **Settings → Pages → Source: GitHub Actions**. The workflow overrides `baseURL` with the real Pages address, so nothing needs changing in `hugo.toml`.

Keep the `HUGO_VERSION` in the workflow in step with the version you use locally.

## Layout

```
hugo.toml            site config, nav, footer links
content/             the pages (markdown)
layouts/             templates: baseof, home, projects/page, plus two shortcodes and an image hook
assets/css/style.css the only stylesheet (minified and fingerprinted at build)
static/              favicon and images, copied as is
archetypes/          scaffold used by `hugo new projects/...`
```
