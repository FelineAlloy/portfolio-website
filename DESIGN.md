---
name: Luxin Matasaru
description: A researcher's catalogue on warm paper. One sans, one deep accent, work grouped by field.
colors:
  paper: "#F8F7F2"
  plate: "#EEECE4"
  ink: "#171715"
  ink-soft: "#3B3A35"
  muted: "#625F57"
  line: "#E2DFD5"
  line-strong: "#C9C5B8"
  control-line: "#8C897F"
  fern: "#2C6E2F"
  fern-strong: "#215223"
  fern-wash: "#E2E8DD"
  mount: "#EAEDE4"
  mount-hover: "#D9E2D5"
  band: "#E6EBE0"
  paper-dark: "#131312"
  plate-dark: "#1D1D1B"
  ink-dark: "#EEEDE7"
  ink-soft-dark: "#CFCDC5"
  muted-dark: "#A3A097"
  line-dark: "#2B2A27"
  line-strong-dark: "#45433E"
  control-line-dark: "#726F69"
  fern-dark: "#86C987"
  fern-strong-dark: "#AAD9AB"
  fern-wash-dark: "#212920"
  mount-dark: "#1E201D"
  mount-hover-dark: "#222722"
  band-dark: "#252D24"
typography:
  display:
    fontFamily: "Hanken Grotesk, ui-sans-serif, system-ui, -apple-system, Segoe UI, sans-serif"
    fontSize: "clamp(2.5rem, 1.9rem + 3vw, 4rem)"
    fontWeight: 600
    lineHeight: 1.02
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Hanken Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2rem, 1.6rem + 1.8vw, 2.75rem)"
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: "-0.03em"
  title:
    fontFamily: "Hanken Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.375rem"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.015em"
  lede:
    fontFamily: "Hanken Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.1875rem"
    fontWeight: 400
    lineHeight: 1.6
  body:
    fontFamily: "Hanken Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Hanken Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.45
    fontFeature: "tnum"
  mono:
    fontFamily: "ui-monospace, SF Mono, Menlo, Consolas, monospace"
    fontSize: "0.875em"
rounded:
  hairline: "2px"
  code: "4px"
  plate: "6px"
  pill: "999px"
spacing:
  "1": "0.25rem"
  "2": "0.5rem"
  "3": "0.75rem"
  "4": "1rem"
  "5": "1.5rem"
  "6": "2rem"
  "7": "3rem"
  "8": "4.5rem"
  "9": "6rem"
components:
  button:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0.5rem 1.125rem"
    height: "2.5rem"
  button-primary:
    backgroundColor: "{colors.fern}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    padding: "0.5rem 1.125rem"
    height: "2.5rem"
  button-primary-hover:
    backgroundColor: "{colors.fern-strong}"
    textColor: "{colors.paper}"
  entry-media:
    backgroundColor: "{colors.mount}"
    rounded: "{rounded.plate}"
    padding: "7%"
  entry-media-hover:
    backgroundColor: "{colors.mount-hover}"
  site-header:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    height: "3.75rem"
  code-block:
    backgroundColor: "{colors.plate}"
    rounded: "{rounded.plate}"
    padding: "1rem"
---

# Design System: Luxin Matasaru

## Overview

**Creative North Star: "The Researcher's Catalogue"**

The site is a catalogue, not a landing page. A visitor learns who Luxin is in one glance (name, affiliation, a short bio, the CV / Email / GitHub pills) and then scans the work grouped by field: years, outcomes and evidence links on every entry, figures mounted on pale fern board where a real figure exists, plain text entries where it does not. The register is warm but academically professional: warm paper, near-black ink, one deep accent, one sans-serif throughout.

Density is calm and list-like. Structure comes from hairline rules and whitespace, never from boxes, cards or shadows. Ornament is absent on purpose: no like or view counts, no badges, no counters, no handwritten type. Content is never invented; a gap stays visible as `TODO` rather than being filled with plausible copy.

The theme follows the visitor's OS setting (`prefers-color-scheme`); dark backgrounds stay near-neutral. The single accent is fern green, a true leaf green chosen by the owner over bottle green, ink blue and viridian.

**Key Characteristics:**
- Warm paper ground, near-black ink, warm grey secondary text.
- One accent, fern green, with fixed jobs: links, results, focus, the primary action, figure mounts and the closing contact band.
- Hanken Grotesk, self-hosted, regular / medium / semibold; no second family except a system mono for code.
- Hairline-topped entries in an auto-fill grid; card figures fill their 3:2 frame, cropped to fit; project-page figures are shown whole.
- Pill-shaped actions; flat surfaces.
- Every browser surface themed: selection, focus ring, link underline offset, tabular numerals, table scrollbar.

## Colors

A warm, low-chroma paper-and-ink neutral set carrying a single deep accent that is swapped by config, never mixed.

### Primary
- **Fern Green** (`fern`): links, results, focus rings, the filled primary pill (CV), and entry-title hover. Its strong step (`fern-strong`) is link and primary-pill hover; its wash (`fern-wash`) is text selection. Dark mode lifts it to a soft leaf green (`fern-dark`).

### Neutral
- **Warm Paper** (`paper`): page ground, sticky header ground, text on primary pills.
- **Fern Mount** (`mount`): paper with 7% fern; the board behind figure thumbnails, project-page figures and videos. Hover deepens it to `mount-hover`.
- **Fern Band** (`band`): paper with 9% fern; the full-width contact footer, so the page closes on color. In dark mode it is one visible step above paper (1.3:1), still near-neutral.
- **Plate** (`plate`): one step deeper than paper, neutral; inline code, code blocks and the portrait's loading ground.
- **Ink** (`ink`): headings, entry titles, primary pill fill, strong text.
- **Soft Ink** (`ink-soft`): body copy, bio, ledes, entry summaries.
- **Warm Grey** (`muted`): meta lines, captions, nav links, evidence links, table headers, list markers.
- **Hairline** (`line`): header rule, table row rules, horizontal rules. Home sections have no rule; space and the section title separate them.
- **Strong Hairline** (`line-strong`): entry top rules, table header rule, blockquote rule, table scrollbar.
- **Control Line** (`control-line`): pill outlines; darker than the hairlines so an outlined action holds 3:1 against paper (3.3 light, 3.7 dark).
- The `-dark` neutrals replace these one for one under `prefers-color-scheme: dark`; they stay near-neutral with only a trace of warmth.

### Named Rules
**The One Accent Rule.** Fern green is the only chromatic color. Everything else is paper, ink or a fade of ink; images bring their own color.

**The Accent Means Something Rule.** Fern has fixed jobs: what acts (links, the primary action, focus), what matters (results), where the page ends (the contact band) and what is evidence (figure mounts). Headings, body text and meta stay ink and grey.

**The Swap Only The Accent Rule.** Switching palettes changes `--accent`, `--accent-strong` and `--accent-wash` and nothing else; neutrals, type and layout are shared.

## Typography

**Display Font:** Hanken Grotesk (with ui-sans-serif, system-ui, -apple-system, Segoe UI, sans-serif)
**Body Font:** Hanken Grotesk (same stack)
**Label/Mono Font:** ui-monospace, SF Mono, Menlo, Consolas (code only)

**Character:** One humanist-leaning grotesk does every job, self-hosted as a variable font (400 to 700, latin and latin-ext subsets). Hierarchy comes from size, weight (400 / 500 / 600) and tight negative tracking on large sizes, not from a second family.

### Hierarchy
- **Display** (600, fluid up to 4rem, 1.02, -0.035em): the name in the home intro only.
- **Headline** (600, fluid 2rem to 2.75rem, 1.1, -0.03em): project page titles.
- **Section** (600, fluid 1.5rem to 1.875rem, 1.15, -0.025em): home section titles (work groups, Experience); with no rules between sections, the title carries the break.
- **Title** (600, 1.375rem, 1.2, -0.015em): prose h2, footer "Contact".
- **Lede** (400, 1.1875rem, 1.6): bio (60ch measure), affiliation (muted, 1.45), project ledes, footer email (500).
- **Body** (400, 1.0625rem, 1.6): prose, in a 42rem reading column. Entry titles use this size at 600 and 1.35; entry summaries step down to 0.9375rem at 1.55.
- **Label** (400, 0.875rem): meta lines (year, role), captions, evidence links, table headers (600). Meta uses tabular numerals. Results use this size at 600 in the accent.

### Named Rules
**The One Family Rule.** Hanken Grotesk everywhere: headings, nav, labels, body. No handwritten, serif or display face; mono is for code alone.

**The Balanced Heading Rule.** Headings use `text-wrap: balance`, paragraphs `text-wrap: pretty`.

**The Justified Text Rule.** Running text (bio, ledes, project prose and list items, experience details) is fully justified with automatic hyphenation from 40rem up. Card summaries, captions and meta stay left-aligned, and so does everything on phone-width screens, where justified lines open visible gaps.

## Layout

A centered shell of 72rem plus a fluid gutter (clamp 1rem to 2.5rem). Spacing is a 4px-based scale (`spacing.1` to `spacing.9`); large section gaps use 3rem to 6rem.

- **Header:** sticky, 3.75rem tall, paper ground with a bottom hairline; name left, nav right. `scroll-padding-top` clears it for anchor jumps.
- **Home intro:** a single column by default; at 52rem and up, when a portrait exists, the text column with the portrait beside it on the right: an 18rem-wide 4:5 photo with the plate radius. Below 52rem it shrinks to 7.5rem and sits above the name. Vertical padding is fluid (3rem to 7rem top).
- **Work groups:** each group opens with its title, no rule; entries sit in an auto-fill grid with a 15.5rem minimum track (four across at full width), 3rem row gap, 1.5rem column gap. Groups are separated by 4.5rem.
- **Entries:** each starts on a strong hairline so rows align when figure and text entries mix.
- **Project page:** header and prose share the 42rem measure; header ends on a hairline.
- **Narrow screens (max-width 40rem):** work grids drop to one column; figure entries become rows with a 5.5rem square thumbnail (cropped to fill) beside the text; tables tighten (0.8125rem, smaller cell padding, wrapping headers).
- **Experience page:** an 11rem dates column beside the roles at the reading measure; each role closes on a hairline, and the page header rule runs the same full width. Stacks on narrow screens.
- **Awards page:** the same 11rem year column beside the awards, one compact row each on a hairline (1rem padding), newest first; the head rule runs the full width. Stacks on narrow screens.
- **Footer:** 6rem above, a full-width fern band, contact block left (every address with its institution, then the pill links), copyright right, wrapping on small screens.

## Elevation & Depth

Flat. No shadows anywhere in the current build. Depth is tonal: figures, thumbnails and video sit on pale fern mounts and code on a neutral plate, both one step from paper, and hairlines separate everything else. Hover responds with tone (the mount deepens) and a 1.025 scale on the figure, not lift. Flatness is the current state rather than a hard prohibition; any future shadow should stay ambient and rare.

## Shapes

Gently rounded rectangles (6px) for plates, figures, videos, the portrait and code blocks; 4px for inline code; 2px for focus-ring corners. Actions are full pills (999px). Rules are 1px hairlines in two weights. Card figures fill a 3:2 frame edge to edge (cropped to fit); project-page figures are never cropped.

## Components

### Buttons (pill links)
Quiet, outlined pills that read as actions, not banners.
- **Shape:** full pill (999px), min height 2.5rem, 0.5rem by 1.125rem padding, 0.9375rem medium text, 0.4em gap to icon or note.
- **Default:** transparent with a `control-line` outline and ink text; hover darkens the outline to ink. The "PDF" note on the primary pill keeps the full paper color.
- **Primary:** fern fill, paper text (used for the CV, the one filled action); hover deepens to the strong fern.
- **Extras:** a small muted file-type note ("PDF", 0.75rem medium) after PDF links; an inline 1em arrow-up-right SVG after external links.
- **Transitions:** border, background and color over 160ms with a soft ease-out (`cubic-bezier(0.22, 1, 0.36, 1)`).

### Links
Accent colored with a 1px underline at 45% of the text color, offset 0.2em; hover moves to the strong accent and a full-strength underline. Evidence links and nav links are muted and turn accent or ink on hover.

### Navigation
Sticky header with the name (ink, 600, -0.01em) and a wrapping list of muted 0.9375rem links (Work, Experience, Awards, CV, Contact); on narrow screens the nav wraps below the name; links turn ink on hover. The current page (Experience) or section (Work, on project pages) carries `aria-current` and shows in ink with a 1px accent underline. Skip link appears on focus as an ink pill-cornered tab.

### Work Entry (signature)
The unit of the catalogue.
- **Structure:** strong hairline top, optional mounted figure, title (ink, 600), meta line (muted, tabular), summary (soft ink), result (accent, 600), evidence links row (muted, separated by middots).
- **Figure:** 3:2 frame with the 6px radius, image covering it edge to edge (cropped to fit; the mount color shows only while it loads); entries without an `image` are text entries.
- **Interaction:** the title link stretches over the whole entry, so the entry is one click target while its accessible name stays the title; evidence links are stacked above it and stay independently clickable. Hover deepens the mount, scales the figure 1.025 and turns the title accent; focus draws the accent ring around the whole entry. Reduced motion removes the transitions and scale.
- **External:** titles linking off-site carry the arrow-up-right icon.

### Experience
- **Role (experience page):** period (muted, tabular) on the left; organisation and position in one heading (organisation as a title, position muted below it), then the role's bullet points with solid disc markers.
- **Summary (home page):** after the work groups, a titled list of rows (position, organisation in 600 on the left, period on the right) on strong hairlines, each linking to its role on the experience page; an "All details" link with an arrow-right icon sits beside the title.

### Award
- **Row (awards page):** year (muted, tabular) on the left; the event as a heading in ink at body size (600), linked to its project page or official results when one exists (ink, accent on hover); the award below it as an accent result.

### Intro Actions
Pill links (CV, GitHub) followed by the primary email address as a plain medium-weight accent link, in one wrapping row.

### Project Page Header
Back link (muted, arrow-left icon), headline title, meta line, lede, result in accent, pill links row; capped at the reading measure and closed by a hairline.

### Prose Figures, Video, Gallery, Tables
- **Figures:** on the fern mount, 6px radius, muted 0.875rem caption below; capped at 75% of the viewport height so portrait photos stay within one screen.
- **Video:** up to 26rem wide; an optional pixelated rendering keeps low-resolution footage sharp.
- **Gallery:** wrapping grid of photos (14rem minimum track, two across in the reading column); `pixelated=true` switches to small 6rem tiles with pixelated scaling for low-resolution frames.
- **Tables:** wrapped in a focusable scroll region with a thin themed scrollbar; muted semibold headers on a strong rule, hairline row rules, tabular numerals, bold cells in accent; tighten on narrow screens and scroll when still too wide.
- **Code:** plate background, system mono; blocks scroll horizontally.

## Do's and Don'ts

### Do:
- **Do** take every color, size and space from the tokens in `assets/css/tokens.css`.
- **Do** change the accent only through the `--accent*` tokens, light and dark together.
- **Do** let the theme follow `prefers-color-scheme` and keep dark grounds near-neutral.
- **Do** fill card frames with real figures (3:2, cropped to fit) and show project-page figures whole and leave entries without a figure as text entries.
- **Do** give every entry its evidence links and set outcomes as accent results.
- **Do** use hairlines and whitespace to separate content.
- **Do** keep icons as inline 1em stroke SVGs in the current text color.
- **Do** honor `prefers-reduced-motion` for any transition or scroll behavior.

### Don't:
- **Don't** add like or view counts, badges, counters or similar gimmicks.
- **Don't** use a handwritten, serif or second display font.
- **Don't** crop figures on project pages or invent placeholder imagery.
- **Don't** show both accent palettes on one page.
- **Don't** put the accent on headings, body text or meta, or add fern regions beyond the mounts and the contact band.
- **Don't** invent content; unverified facts are written as `TODO`.
