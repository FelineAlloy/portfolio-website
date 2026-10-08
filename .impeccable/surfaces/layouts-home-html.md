---
version: 1
slug: "layouts-home-html"
primary_target: "layouts/home.html"
related_targets: ["layouts/projects/page.html"]
---

# Surface: home page and project pages (whole site)

Scope: the home page (`layouts/home.html`) and project pages (`layouts/projects/page.html`), rebuilt from scratch as one system. Mode: Experience (the work leads), for research supervisors and admissions reviewers doing a one-minute credibility check.

Pinned by the owner: same general direction as before (warm, academic, light), modelled on antonioterpin.com (warm paper, one sans, deep accent, flat lists, pill actions) and josephdelpreto.com (image-led project cards grouped by relevance). One sans throughout. Accent: two independent palettes (green, ink blue) switchable by config; owner chooses after seeing both. Email luxin.matasaru@polytechnique.edu; portrait slot that renders only when a photo exists. Code must be modular and easy to extend. No gimmicks. Concept-seed roll skipped: direction pinned by the brief.

## Direction contract

THESIS: A researcher's catalogue, not a landing page: who Luxin is in one glance, then the work grouped by field, figures mounted on plates where a real figure exists and text entries otherwise, every entry showing its evidence links. Refuses the template hero-plus-equal-cards and the dark dev-portfolio.

OWN-WORLD: Warm paper ground (#F8F7F2) with a slightly deeper plate tone for figure mounts, near-black ink, warm grey secondary, one deep accent, fern green (#2C6E2F), used for links, results and focus. Hanken Grotesk, self-hosted, in three weights. Figures sit contained on paper-tone plates with a 6px radius; hairline rules; pill-shaped actions; no shadows.

STORY: The visitor reads name, affiliation and a three-sentence bio, sees CV / Email / GitHub immediately, scans grouped work with years and outcomes, and opens the one that matters to them; each project page leads with its evidence links.

FIRST VIEWPORT: Sticky thin header (name left; Work, CV, Contact right). Intro on a 12-column grid: name set fluid up to 4rem (amended from 3.5rem: the built size holds the line better at 1440), affiliation line under it, bio at a 60ch measure, then the action pills; portrait in the right four columns when present. The first work group's heading begins at the bottom of the viewport on desktop.

FORM: Pinned by the brief (catalogue after the two references); first on my list. No seed key: the roll was skipped because the owner pinned the direction ("redesign the website from the ground up while keeping the same general direction ... A good example is https://antonioterpin.com/#about"; cards "like here https://www.josephdelpreto.com/"). Disclosed to the owner.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance

## Open decisions
- Accent: decided, fern green (owner chose it over viridian after seeing both on the site).
- Portrait photo, thumbnails for imageless entries: owner supplies.
