# Gordon Lab Website — Claude Context

This project is a static academic lab website for the Gordon Lab at Rutgers University,
built with Hugo and deployed via GitHub Pages.

## PI

**Adam Gordon-Fennell, Ph.D.**
Assistant Professor (tenure-track), Department of Psychology, Rutgers University
Start date: September 2026
Email: adam.g.gordon@rutgers.edu
Office: Psychology Bldg 223, Busch Campus
Google Scholar: https://scholar.google.com/citations?user=aVheI74AAAAJ&hl=en

## Research focus

Circuit neuroscience of behavior — specifically the lateral hypothalamus (LHA) and
dopamine (DA) circuits mediating positive/negative reinforcement, with implications
for substance use disorder (SUD). Key techniques: 2-photon calcium imaging,
multi-site fiber photometry, optogenetics, head-fixed behavioral paradigms, GLMs.

## Key files

| Path | Purpose |
|------|---------|
| `hugo.toml` | Site config — title, baseURL, nav menus |
| `layouts/` | Hugo templates (HTML structure) |
| `layouts/_default/` | Base templates used across pages |
| `layouts/partials/` | Reusable components (header, footer, nav) |
| `content/` | Markdown source files for every page |
| `static/` | Images, PDFs, fonts, raw CSS/JS |
| `assets/css/` | Main stylesheet(s) |
| `source_documents/` | PI's CV, research statement, general info — NOT deployed |

## Local development

```bash
# Install Hugo (once)
brew install hugo

# Serve locally with live reload
hugo server -D

# Build for production
hugo
```

The built site goes to `public/` — GitHub Actions deploys this automatically on push to `main`.

## Site pages

| URL | Content file | Purpose |
|-----|-------------|---------|
| `/` | `content/_index.md` | Home — hero, one-liner, 3 research pillars |
| `/research/` | `content/research/_index.md` | Research areas (3 projects) |
| `/people/` | `content/people/_index.md` | Team — PI bio + future members |
| `/publications/` | `content/publications/_index.md` | Paper list with abstracts, figures, PDF links |
| `/news/` | `content/news/` | Blog-style news posts |
| `/join/` | `content/join/_index.md` | Prospective students and postdocs |
| `/contact/` | `content/contact/_index.md` | Email, office, links |

## Design decisions

- **Color accent:** TBD — placeholder is a deep teal (#1a6b6b) until PI decides
- **Style:** Clean multi-page (not single-scroll), modern sans-serif typography
- **Publications page:** Title, authors, journal, abstract, key figures (no verbose captions), PDF link
- **Reference sites liked:** Parker Lab (visual style), Calipari Lab (publications format)
- **Reference sites disliked:** Barker Lab (style), Parker Lab single-scroll layout

## Deployment

- GitHub repo: TBD (will be created during Phase 1)
- Hosting: GitHub Pages (free)
- Domain: TBD — may add custom domain later
- Deploy method: GitHub Actions workflow (`.github/workflows/deploy.yml`)

## Content sources

Raw content to draw from is in `source_documents/`:
- `gordon_cv.md` — full publication list, grants, presentations, mentorship
- `gordonfennell_rutgers_research.md` — 3 research projects with background
- `general_info.md` — contact info, Google Scholar
