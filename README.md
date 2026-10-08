# Portfolio website

A small, static research portfolio built with [Hugo](https://gohugo.io) and hosted on GitHub Pages. No npm, no CSS framework, no JavaScript: the only tool is the `hugo` binary. Every page is a markdown file.

## Run locally

Install Hugo (standard edition, v0.166 or newer), then:

```sh
hugo server        # live preview at http://localhost:1313
hugo server -D     # also show drafts
```

## Edit content

| To change | Edit |
|---|---|
| Name, affiliation line, bio, portrait | `content/_index.md` |
| Email addresses, CV/GitHub/LinkedIn buttons, nav | `hugo.toml` |
| The groups on the home page and their order | `data/groups.toml` |
| An internship or job (Experience page) | `content/experience/<slug>.md` |
| A project or experience | `content/projects/<slug>.md` or `content/projects/<slug>/index.md` |

**Add a project or experience**

```sh
hugo new projects/my-project.md            # an entry without images
hugo new projects/my-project/index.md      # an entry with images, PDFs or videos next to it
```

Fill in the front matter (the template explains every field) and delete `draft: true`. The entry appears on the home page in its `group`, ordered by `weight`. An entry with a body gets its own page; an entry with `build: render: never` is a card only, linking to its first link.

**Add a role to the Experience page:** create `content/experience/<slug>.md` with `title` (position), `org`, `period` and `date` (sorts newest first) in the front matter, and the details as a bullet list. It appears on the Experience page and in the home page summary.

**Email addresses:** `params.emails` in `hugo.toml`. The first is shown in the intro; all are listed under Contact with their institution.

**Add a group:** add a `[[groups]]` block to `data/groups.toml` and use its `id` in entries. The build warns about entries whose group is not listed.

**Portrait:** `assets/img/portrait.jpg`, set by `portrait` in `content/_index.md`. Hugo crops it to 4:5 and resizes it at build, so any reasonably large photo works. (Don't put files in `resources/`: that is Hugo's cache and gets cleaned.)

**Card images:** set `image:` to a file next to the entry. It is shown whole on a mounted plate, never cropped. Entries without an image are text entries, so adding one later needs no other change.

**Colors:** all in `assets/css/tokens.css`, light and dark. The accent is fern green (`--accent`).

**Markdown features**

- Standard markdown: headings, lists, links, tables, footnotes, code blocks (plain, no highlighting).
- `![alt](file.png "caption")` on its own line becomes a figure with a caption. The file can sit next to the page or under `static/` with a leading slash.
- Tables scroll sideways on small screens.
- `{{< gallery >}} …images, one per line… {{< /gallery >}}` lays images out in a grid.
- `{{< video src="file.mp4" caption="…" >}}` embeds a video; add `pixelated=true` for low-resolution footage.
- Raw HTML is disabled. For links to other pages of this site, use `{{< relref "projects/slug" >}}`.

## Deploy

Pushing to `main` runs `.github/workflows/hugo.yml`, which builds the site and publishes it. One-time setup: in the GitHub repo, **Settings → Pages → Source: GitHub Actions**. The workflow overrides `baseURL` with the real Pages address, so nothing needs changing in `hugo.toml`.

Keep the `HUGO_VERSION` in the workflow in step with the version you use locally.

## Layout

```
hugo.toml               site config: links, emails, nav
data/groups.toml        home page groups
content/                pages (markdown): projects/ holds the work entries, experience/ the roles
layouts/
  baseof.html           page skeleton
  home.html             intro + groups
  projects/page.html    an entry's own page
  experience/section.html   the Experience page
  404.html
  _partials/
    site/               head, header, footer
    home/               intro, group, experience summary, build-time group check
    work/               entry card, meta line
    experience/         one role
    links.html          pill link row
    icon.html           inline SVG icons
    func/resolve-url.html   turns any link into one that works under the Pages sub-path
  _markup/              image and table render hooks
  _shortcodes/          gallery, video
assets/css/             one file per concern, bundled in the order listed in _partials/site/head.html
static/                 fonts, CV, files copied as is (the site icon is generated from the portrait)
archetypes/projects.md  template used by `hugo new projects/...`
```

## Hugo 0.166 notes

- Layout folders use the new names: `_partials/`, `_shortcodes/`, `_markup/`, `home.html`, `projects/page.html`.
- `relURL` leaves `/path` untouched (only `/` and fragments get the base path). Strip the leading slash first, as `func/resolve-url.html` does.
- Menu URLs are lowercased by Hugo, so nav links live in `params.href` on each menu entry.
- `hugo.toml` has `baseURL = "/"` for local preview; CI passes the real one.
