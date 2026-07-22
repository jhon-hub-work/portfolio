<h1 align="center">Portfolio — Jhon Buerano</h1>

<p align="center">
  <strong>A conversion-first portfolio and long-form engineering case study.</strong><br/>
  Hand-written HTML, CSS, and JavaScript. No framework, no build step, no dependencies.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-1a1a1a?style=flat-square&logo=html5&logoColor=E34F26" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1a1a1a?style=flat-square&logo=css3&logoColor=1572B6" alt="CSS3"/>
  <img src="https://img.shields.io/badge/Vanilla_JS-1a1a1a?style=flat-square&logo=javascript&logoColor=F7DF1E" alt="Vanilla JS"/>
  <img src="https://img.shields.io/badge/Netlify-1a1a1a?style=flat-square&logo=netlify&logoColor=00C7B7" alt="Netlify"/>
  <img src="https://img.shields.io/badge/build_step-none-1F883D?style=flat-square" alt="No build step"/>
</p>

<p align="center">
  <a href="https://jhonmbuerano.netlify.app"><strong>Live site</strong></a> ·
  <a href="https://wave3-portfolio.netlify.app"><strong>Wave3 case study</strong></a>
</p>

---

## Overview

Two pages with one job each:

- **`index.html`** — the portfolio. Positioning, featured work, and a booking CTA.
- **`wave3-case-study.html`** — a long-form engineering case study on [Wave3 Collective](https://github.com/jhon-hub-work/wave3), covering the business context, the architecture, and the decisions behind it.

## Problem

A developer portfolio has roughly fifteen seconds to answer one question: *can this person ship
something real?* Most portfolios answer a different question — what technologies does this person
know — and lose the reader before any evidence arrives.

## Constraints

| Constraint | Consequence |
|---|---|
| Reader gives it seconds, not minutes | Proof of shipped work sits above the fold; the stack list is secondary |
| Must load instantly on Philippine mobile data | No framework, no bundle, no hydration — HTML that renders on arrival |
| Static hosting only | Everything is a flat file; no server, no runtime |
| Solo maintenance | Zero dependencies means zero dependency upgrades, ever |

## Engineering Decisions

| Chosen | Over | Why |
|---|---|---|
| Hand-written HTML/CSS/JS | React / Next.js / Astro | Two static pages. A framework adds a build step, a dependency tree, and bundle weight in exchange for component reuse this site has no need of. |
| No build step | Vite / bundler pipeline | What you read in the repo is byte-for-byte what runs in production. Nothing to break, nothing to rebuild years from now. |
| Semantic HTML + JSON-LD | Framework SEO plugins | Structured data and meta tags are a handful of lines written directly, not a plugin to configure and keep current. |
| Netlify static hosting | A Node server | Nothing here needs a runtime. Static hosting is faster, free, and has no attack surface to maintain. |
| Case study as its own page | A section on the homepage | The two readers are different: one is skimming for credibility, the other is already interested and wants depth. Splitting them lets each page be honest about its length. |

The same constraint discipline as the projects it showcases: every dependency has to earn the cost
of operating it alone.

## Folder Structure

```
index.html                  Portfolio — hero, work, positioning, booking CTA
wave3-case-study.html       Long-form Wave3 engineering case study
Jhon-Buerano-Resume.pdf     Resume, linked from both pages
*.jpg                       Screenshots of Wave3 (storefront, admin, mobile)
```

Flat on purpose. Two pages and their assets do not need a directory tree.

## Running Locally

No install, no build:

```bash
# open directly
start index.html

# or serve it, if you want correct relative paths and no file:// quirks
npx serve .
```

## Deployment

Netlify, deployed from this repository. No build command, no environment variables — the publish
directory is the repository root.

## Roadmap

- [ ] Real client testimonials (placeholder section is commented out until quotes are genuine)
- [ ] Case studies for the salon booking platform and the AI automation client work
- [ ] Compress and convert screenshots to WebP with `<picture>` fallbacks
- [ ] Lighthouse pass — target 100 across performance, accessibility, and SEO
- [ ] Replace the inline SVG favicon with a proper icon set

## Lessons Learned

- **Positioning beat polish.** The version that read "Full Stack Developer" performed worse than the one naming the actual outcome — platforms non-technical owners run without a developer. Same code, different sentence.
- **A case study is worth more than a project grid.** One project explained in depth — why it exists, what was traded away, what broke — does more than six thumbnails.
- **No build step is a feature over time.** This site will still deploy unchanged in five years. Every framework portfolio I've seen from five years ago needs work before it will build at all.

## License

All rights reserved. The code is public to be read; the writing, branding, and imagery are not for reuse.

---

<p align="center">
  <sub>Designed, built, and written by <strong>Jhon Buerano</strong>.</sub><br/>
  <sub><a href="https://jhonmbuerano.netlify.app">Portfolio</a> · <a href="https://www.linkedin.com/in/jhon-mycho-buerano">LinkedIn</a></sub>
</p>
