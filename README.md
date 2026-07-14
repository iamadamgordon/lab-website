# Gordon Lab Website

Academic lab website for the Gordon Lab, Department of Psychology, Rutgers University.

**PI:** Adam Gordon-Fennell, Ph.D.
**Research:** Circuit neuroscience of behavior — LHA and dopamine circuits of reinforcement and substance use disorder
**Live site:** TBD (GitHub Pages)

## Tech stack

- [Hugo](https://gohugo.io/) — static site generator
- GitHub Pages — free hosting
- Custom theme — built to match the lab's visual identity

## Local development

```bash
# Prerequisites: Hugo installed (brew install hugo on Mac)

# Clone the repo
git clone <repo-url>
cd website-lab

# Start local server with live reload
hugo server -D

# Open http://localhost:1313 in a browser
```

## Project structure

```
website-lab/
├── hugo.toml              # Site configuration
├── content/               # Page content (Markdown)
│   ├── _index.md          # Home page
│   ├── research/
│   ├── people/
│   ├── publications/
│   ├── news/
│   ├── join/
│   └── contact/
├── layouts/               # HTML templates
│   ├── _default/
│   └── partials/          # Header, footer, nav, pub card, etc.
├── static/                # Images, PDFs, fonts
├── assets/css/            # Stylesheets
└── source_documents/      # Raw content (not deployed)
```

## Adding content

**New publication:** Edit `content/publications/_index.md` — add an entry following the existing format (title, authors, journal, year, abstract, PDF path, figure paths).

**News post:** Create `content/news/YYYY-MM-DD-title.md` with frontmatter `title`, `date`, `summary`.

**New team member:** Edit `content/people/_index.md` and add a photo to `static/images/people/`.

## Deployment

Pushing to `main` triggers a GitHub Actions workflow that builds the site and deploys `public/` to GitHub Pages. No manual steps needed.

## Source documents

The `source_documents/` folder contains the PI's CV, research statement, and contact info. These are the source of truth for content but are not deployed to the site.
