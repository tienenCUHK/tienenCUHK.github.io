# Design Spec: Academic Personal Homepage

**Date:** 2026-07-19  
**User:** tienenCUHK (GitHub)  
**Domain:** AI for Science / PhD Student  
**Stack:** GitHub Pages + Jekyll + al-folio theme

---

## 1. Overview

Deploy a complete academic personal homepage at `https://tienenCUHK.github.io` using the al-folio Jekyll theme. The site follows a minimalist academic visual style — black & white with subtle blue accents, serif headings, generous whitespace.

## 2. Site Structure

| Page | Route | Content |
|------|-------|---------|
| Home | `/` | Photo, short bio, research interests, latest news, contact/social links |
| Publications | `/publications/` | Papers by year, BibTeX popups, PDF links, venue badges |
| Projects | `/projects/` | Research project cards with image, description, GitHub links |
| Blog | `/blog/` | Technical posts in Markdown, organized by year and tags |
| CV | `/cv/` | Embedded PDF download + education/experience summary |

Navigation: Fixed top bar (Home · Publications · Projects · Blog · CV), footer with social icons.

## 3. Visual Design

- **Style**: Minimalist academic — white background, black/dark-gray text, deep blue (`#003366`) links
- **Typography**: System sans-serif for body, serif (Georgia) for headings
- **Layout**: Single-column, max-width 800px, left-aligned, generous margins
- **Components**: Thin-bordered cards, subtle separators, rounded corners (4px)
- **Dark mode**: Auto-detected from system preference (al-folio built-in)
- **Responsive**: Mobile-friendly via al-folio

## 4. Technical Architecture

- **Theme**: [al-folio](https://github.com/alshedivat/al-folio) — Jekyll-based academic theme
- **Deployment**: GitHub Pages, push to `main` → auto-build
- **Content format**: Markdown for pages/posts, BibTeX for publications, YAML for config
- **Key features**: Dark mode, KaTeX math, full-text search, Google Analytics ready, responsive images

## 5. Required User Data

- [ ] Professional headshot (~400×400px)
- [ ] Full name, affiliation, email
- [ ] Research interests (3–5 bullet points)
- [ ] Short bio paragraph
- [ ] Publications .bib file (export from Google Scholar / DBLP)
- [ ] CV PDF file
- [ ] Social links (Google Scholar, GitHub, Twitter/X, ORCID, etc.)
- [ ] Project descriptions and screenshots (optional, can add later)

## 6. Content Strategy

- **Home page**: Bio + interests + news — update every few months with new milestones
- **Publications**: Import from Google Scholar BibTeX, update when new papers accepted
- **Projects**: 2–4 featured projects; each with a screenshot, 2-3 sentence description, and link
- **Blog**: Optional; post when you have something to share (paper summaries, tutorials, conference reports)
- **CV**: Keep the PDF current; al-folio can generate an HTML version from structured data

## 7. Future Enhancements (out of scope for v1)

- Custom domain (e.g., `yourname.com`)
- Google Analytics integration
- Altmetrics badges on publications
- Teaching / mentorship page
- Interactive research visualizations
