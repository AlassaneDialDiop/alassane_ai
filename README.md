# alassane.ai — v2

Personal site for Alassane Diop, AI Engineer. Rebuilt 2026-06 — dark engineer-minimal design, zero build step.

## Stack

Plain HTML + CSS + vanilla JS. No Jekyll, no Ruby, no npm, no build pipeline.
Why: GitHub Pages serves static files directly; a build step was solving a problem this site doesn't have. Editing a page = editing one HTML file.

## Structure

```
index.html                  Home: hero, proof strip, work, testimonial, writing, contact
about/index.html            Story, timeline, education, toolbox
work/{vibecope,olima,tastet,browns}/index.html    Case studies
writing/index.html          Post list
writing/<slug>/index.html   Posts (drafts marked with DRAFT badge — remove the
                            <span class="draft-badge"> when published)
assets/css/style.css        The entire design system (CSS variables at top)
assets/js/main.js           Scroll-reveal only
assets/img/                 Images
assets/resume.pdf           Downloadable resume (NOTE: contains phone number)
CNAME                       alassane.ai custom domain
```

## Local preview

```bash
python3 -m http.server 8000
# visit http://localhost:8000
```

## Deploying

This folder replaces the contents of github.com/AlassaneDialDiop/alassane_ai (main branch → GitHub Pages). The CNAME file must remain at root.

## Editing cheatsheet

- Accent color: `--accent` in style.css (currently amber #e8a94d)
- New post: copy a writing/<slug>/ folder, add a row in writing/index.html and the home page list, add the URL to sitemap.xml
- New case study: copy a work/<slug>/ folder, add a card on index.html
