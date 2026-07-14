# Gordon Lab Website — Roadmap

Goal: launch a polished, multi-page academic lab website on GitHub Pages before
the September 2026 Rutgers start date. Built with Hugo and a custom theme.

---

## Phase 1 — Hugo project setup

**Goal:** A running Hugo project in version control, deployable to GitHub Pages.

- [ ] Install Hugo (`brew install hugo`)
- [ ] Initialize Hugo project in `/Users/adamgordon-fennell/code/website-lab/`
- [ ] Create `hugo.toml` with site title, baseURL, and language settings
- [ ] Scaffold directory structure: `content/`, `layouts/`, `static/`, `assets/`
- [ ] Create a minimal home page (`content/_index.md`) to verify the build works
- [ ] Run `hugo server` locally and confirm the site loads
- [ ] Initialize a GitHub repo (`iamadamgordon/lab-website` or similar)
- [ ] Set up GitHub Actions deploy workflow (`.github/workflows/deploy.yml`)
- [ ] Enable GitHub Pages on the repo (source: GitHub Actions)
- [ ] Push and confirm the bare site is live at `iamadamgordon.github.io/<repo>`

---

## Phase 2 — Page structure and navigation

**Goal:** All pages exist and are reachable via a working nav bar.

- [ ] Create content stubs for all pages:
  - `content/_index.md` (Home)
  - `content/research/_index.md`
  - `content/people/_index.md`
  - `content/publications/_index.md`
  - `content/news/_index.md`
  - `content/join/_index.md`
  - `content/contact/_index.md`
- [ ] Build base layout (`layouts/_default/baseof.html`) with `<head>`, `<body>`, header, footer
- [ ] Build nav partial (`layouts/partials/nav.html`) — logo/name left, links right
- [ ] Build footer partial (`layouts/partials/footer.html`) — email, Google Scholar, copyright
- [ ] Configure nav menu in `hugo.toml`
- [ ] Verify all pages render and nav links work locally

---

## Phase 3 — Visual design

**Goal:** A consistent, professional look matching the PI's style preferences
(clean, modern, multi-page; Parker Lab aesthetic; not single-scroll).

- [ ] Decide on color accent (placeholder: deep teal `#1a6b6b`) — confirm with PI
- [ ] Choose typography: sans-serif body + slightly heavier nav/headings
  - Candidate: Inter or DM Sans (Google Fonts, free)
- [ ] Write base CSS (`assets/css/main.css`):
  - CSS custom properties for colors and typography scale
  - Reset / normalize
  - Layout grid (max-width container, responsive)
  - Nav bar (sticky, clean, links with hover states)
  - Footer
  - Typography defaults
- [ ] Design and implement the home page hero (name, tagline, CTA buttons)
- [ ] Implement responsive behavior (mobile nav hamburger or collapsible menu)
- [ ] Review on mobile and desktop — confirm no horizontal scroll, readable font sizes

---

## Phase 4 — Content: Research page

**Goal:** Communicates the lab's three research projects clearly to a scientific audience
and to prospective students.

Content source: `source_documents/gordonfennell_rutgers_research.md`

- [ ] Write `content/research/_index.md` — 2-sentence lab overview + 3 project sections
  - **Project 1:** LHA and striatal DA encoding in positive/negative reinforcement
  - **Project 2:** LHA and striatal DA during development of opioid motivation (SUD)
  - **Project 3:** Activity-defined clusters of LHA neurons → circuit and behavior
- [ ] Add a "Techniques" section: 2-photon imaging, multi-site fiber photometry, optogenetics, head-fixed behavior, computational approaches (GLMs, ML)
- [ ] Create research page layout template (`layouts/research/list.html`)
- [ ] Add placeholder figures (diagrams or representative microscopy images if available)

---

## Phase 5 — Content: People page

**Goal:** Professional team page. Launch with PI only; structured for easy addition of
future lab members (grad students, postdocs, techs).

Content source: `source_documents/gordon_cv.md`, `source_documents/general_info.md`

- [ ] Write PI bio section: name, title, photo, 3-4 sentence bio, CV link, Google Scholar link
- [ ] Add placeholder cards for "Graduate Students — joining Fall 2026" and "Postdocs"
- [ ] Add "Lab Alumni" section (hidden or minimal at launch; populate later)
- [ ] Add headshot to `static/images/people/gordon-fennell.jpg`
- [ ] Create people page layout template (`layouts/people/list.html`) with photo cards

---

## Phase 6 — Content: Publications page

**Goal:** Calipari Lab-style publications list — each paper shows title, authors, journal,
abstract, 1-2 key figures (no verbose captions), and a PDF download link.

Content source: `source_documents/gordon_cv.md` (PUBLICATIONS section)

Publications to include (most recent first):

**Published:**
- 2026 — Hjort et al., *Nature* (co-author)
- 2025 — Volcko et al., *J. Neurochemistry* (co-author)
- 2024 — Hjort et al., *Neurophotonics* (co-author)
- 2023 — Zhou et al., *Neuron* (co-author)
- 2023 — Gordon-Fennell et al., *eLife* ⭐ first author
- 2021 — Gordon-Fennell & Stuber, *Neuropharmacology* ⭐ first author
- 2020 — Gordon-Fennell et al., *Front. Systems Neuroscience* ⭐ first author
- 2020 — Gordon-Fennell et al., *Front. Neuroscience* ⭐ first author
- 2019 — Pomrenze et al., *Cell Reports* (co-author)
- 2014 — Goldring et al., *J. Neurophysiology* (co-author)

**In revision / preprint (show separately):**
- LHA regulates striatum-wide DA dynamics — in revision at *Neuron* (first author)
- Head-fixed drug self-administration fabrication — in revision at *Nature Protocols* (co-first)
- Endogenous opioid dynamics in dorsal striatum — in revision at *Cell* (co-author)

**Tasks:**
- [ ] Create publication data format (YAML frontmatter in each pub's `.md` file, or a single `data/publications.yaml`)
- [ ] Build publications list template (`layouts/publications/list.html`) — card per paper
- [ ] Build publication card partial: title → authors → journal/year → abstract (expandable or always visible) → figures → PDF link
- [ ] Populate all published papers with abstracts (fetch from DOI pages)
- [ ] Collect PDF files and add to `static/pdfs/`
- [ ] Collect 1-2 key figures per first-author paper, add to `static/images/publications/`
- [ ] Add "In Revision" section above the main list

---

## Phase 7 — Content: News, Join, Contact pages

**Goal:** Fill in the remaining pages so the site feels complete at launch.

**News:**
- [ ] Write 2-3 launch news posts to seed the page:
  - "Gordon Lab opening at Rutgers, Fall 2026"
  - "NIDA K99/R00 award" (if not already public)
  - A notable recent paper highlight
- [ ] Create news list and single templates

**Join:**
- [ ] Write blurb for prospective graduate students (what the lab looks for, how to apply)
- [ ] Write blurb for prospective postdocs (contact info, what to include in email)
- [ ] Write blurb for undergrads / rotation students
- [ ] Note: Rutgers Psychology PhD program application link

**Contact:**
- [ ] Email: adam.g.gordon@rutgers.edu
- [ ] Office: Psychology Bldg 223, Busch Campus, Rutgers University
- [ ] Google Scholar link
- [ ] Embedded map or campus directions (optional)

---

## Phase 8 — Polish and pre-launch review

- [ ] Test all internal links
- [ ] Check all external links (DOIs, Google Scholar, Rutgers pages)
- [ ] Test on mobile (iOS Safari, Android Chrome)
- [ ] Test on desktop (Chrome, Firefox, Safari)
- [ ] Verify PDFs open correctly
- [ ] Check page load speed (`hugo` build output, image sizes)
- [ ] Compress large images (`convert -resize 800x` or similar)
- [ ] Add `<meta>` description tags for SEO on each page
- [ ] Add favicon (`static/favicon.ico` or SVG)
- [ ] Review all text for typos and consistency (lab name, title, institution name)

---

## Phase 9 — Custom domain (optional)

- [ ] Purchase domain (suggested: `gordonneurosciencelab.com` or similar, ~$12/yr via Namecheap or Cloudflare)
- [ ] Add `CNAME` file to `static/` with domain name
- [ ] Configure DNS: CNAME record pointing to `iamadamgordon.github.io`
- [ ] Enable HTTPS in GitHub Pages repo settings
- [ ] Update `baseURL` in `hugo.toml`

---

## Open questions for PI

1. **Color accent:** Any preference, or defer to designer eye? (placeholder: teal)
2. **Lab name on site:** "Gordon Lab" or "Gordon-Fennell Lab"?
3. **Headshot:** Do you have a high-res photo ready?
4. **Publication figures:** Do you have permission/files for key figures from first-author papers?
5. **Domain name:** Do you want a custom domain, or is `github.io` fine for now?
6. **Lab logo:** Want one designed, or just typographic (name in styled font)?
