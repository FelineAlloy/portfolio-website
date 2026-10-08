# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

- **Research supervisors**: professors and lab members deciding whether to take Luxin on for a research internship, thesis or PhD.
- **Admissions committees**: master's or PhD reviewers who followed a link from an application.

Both arrive with context already (a CV, an application, an email) and spend about a minute on the site.

## Product Purpose

A personal research portfolio for Luxin Matasaru, a 3rd-year Mathematics & Computer Science student at École Polytechnique, currently on exchange at ETH Zurich. Interests: machine learning, robotics and engineering, especially for space applications.

Success is a **quick credibility check**: within a minute the visitor confirms the person is real and capable, sees what they have actually built, and can verify it (code, report, results, leaderboard) if they want to.

## Positioning

Every claim is backed by something checkable: a public repo, a report PDF, a results table against the original paper, a competition leaderboard, a PCB layout. The site shows real work across ML research and hardware rather than describing ambitions.

## Operating Context

- Visitors usually come from an application, CV or email, often on a desktop, sometimes on a phone.
- The owner edits markdown and pushes to `main`; GitHub Actions builds with Hugo and publishes to GitHub Pages.

## Capabilities and Constraints

- Hugo static site, standard `hugo` binary (v0.166+) is the only build tool. No npm, no CSS framework; a Hugo theme and small inline JavaScript are allowed. Lightweight is the top priority; ask before adding any other dependency.
- All content is markdown; layout lives in templates. Adding a project must need only one new markdown file (or page bundle). The home page may have its own layout distinct from project pages.
- Stylesheets in `assets/css/` (may be split). The theme follows the visitor's OS preference; dark backgrounds near-neutral, green only as accent.
- Raw HTML in markdown is disabled; shortcodes: `gallery`, `video`.
- Home page: intro, then projects and experiences as cards grouped by relevance (`data/groups.toml`). Entries without a page of their own are card-only.

## Brand Commitments

- Name: Luxin Matasaru. GitHub: FelineAlloy.
- Voice: first person, plain, factual, a little personal (camera, scuba diving). No inflated claims.

## Evidence on Hand

- Projects (`content/projects/`):
  - **QR-DQN for CleanRL** (2026): code, report and defense PDFs, Atari results table vs. the original paper, gameplay video, screenshots, Pong distribution plot. Supervised by Dr. Simo Alami.
  - **Swarm Rescue** (2024): code, leaderboard link, team 14 reached the final round (one of 10 teams), simulation video.
  - **IP Paris Formula Student Racing** (2024–present): BSPD and ready-to-drive circuit design, BSPD PCB image. Start date is still `TODO`.
  - **Diffusion Seminar** (2025): slides PDF, organized with the X CS Committee.
- CV: `static/Resume_Luxin_Matasaru.pdf`, linked from the nav, intro and footer. Card entries for internships, competitions and side projects are drafted from it.
- Public email: luxin.matasaru@polytechnique.edu.
- Approved but not yet supplied: portrait photo, card images for most entries, own photography and dive photos.
- Absent, never to be fabricated: publications, awards, testimonials, Field Notes dates/sites/captions.

## Product Principles

1. **Verifiable over impressive.** Every claim links to its evidence; unknown facts are written `TODO`, never invented.
2. **One-minute read.** Who Luxin is, what they have built, and how to reach them must be clear without scrolling far or clicking around.
3. **Light by construction.** Minimal JS, no npm or frameworks; pages stay small and fast on any connection.
4. **Markdown is the source.** Content lives in markdown, layout in templates; the owner never edits HTML to add work.
5. **Work leads, personality annotates.** The projects carry the page; personal notes stay short margin notes.
