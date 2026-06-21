# From Simulation to Agents — DimensionLab · Ulysseus 2026

Reveal.js lecture deck for the **Ulysseus BIP** virtual session on **22 June 2026**, paired with the in-person mobility in Genoa (29 June – 3 July).

- **Talk title** — *From Simulation to Agents: DimensionLab's Journey in Human-Centred AI for Bioengineering*
- **Audience** — HERO (Human-centred and Ethical Robotics) and AWAKE (Ageing & Well-being) cohorts: engineers, biomedical researchers, clinicians.
- **Speaker** — Michal Takáč, PhD (co-founder, DimensionLab).

The deck is a static folder. Reveal.js, the custom theme, all images, and the demo video are vendored locally. It will open from disk or from any static web server — **no internet required**.

> **CrAInial demo video:** the "See it run." slide plays a local HTML5 video (`assets/videos/crainial-cran-2-1080p.mp4`) with a poster frame at `assets/images/crainial-demo-poster.jpg`. It plays inline whether you open the deck from disk (`file://`) or serve it over HTTP, and works fully offline. The video auto-pauses when you move to another slide. To replace it, drop a new `.mp4` in `assets/videos/` and update the `<source>` on that slide.

## Run locally

You can simply open `index.html` in a modern browser. For full speaker-notes support (a separate window with notes + timer), serve the folder over HTTP — most browsers block the `notes.html` popup when the page is opened with the `file://` scheme.

The simplest local servers:

```bash
# from this directory
python3 -m http.server 8080
# then visit http://localhost:8080/
```

```bash
# or with Node
npx --yes serve -l 8080 .
```

## Speaker notes

Press <kbd>S</kbd> while the deck has focus to open the Reveal.js speaker view in a new window. Notes are embedded inside each slide as `<aside class="notes">`.

## PDF export

Add `?print-pdf` to the URL in a Chromium-based browser, then use the browser's *Print → Save as PDF*. Recommended print settings:

- **Layout** — Landscape
- **Margins** — None
- **Background graphics** — On
- **Paper size** — A4 or US Letter

## Structure

```
deck/
  index.html              # all slides + Reveal.js bootstrap
  styles/theme.css        # DimensionLab white theme on top of Reveal
  assets/
    logos/                # DimensionLab + Siml.ai marks
    images/               # product screenshots, case-study renders
  vendor/reveal.js/       # vendored Reveal.js 5.1.0 (dist + selected plugins)
  README.md
```

## Editing

- **Slides** — edit `index.html`. Slides are plain HTML `<section>` blocks; speaker notes live inside `<aside class="notes">`.
- **Theme** — edit `styles/theme.css`. CSS custom properties at the top control colors, radius, and shadows.
- **Logos** — replace files in `assets/logos/` and update references in `index.html` if needed. The header mark is an inline SVG inside `index.html`.

## Hosting

Any static host works: GitHub Pages, Netlify, Vercel, Cloudflare Pages, S3 + CloudFront, or a USB stick. There is no build step.

## Acknowledgements

- Ulysseus European University Alliance — BIP HERO and BIP AWAKE programmes.
- NVIDIA Modulus and Omniverse — core technologies behind Siml.ai.
- Biomedical Engineering s.r.o. and Prof. Radovan Hudák — clinical partnership for CrAInial.
