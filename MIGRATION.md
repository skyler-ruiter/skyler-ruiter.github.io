# Migration Tasks

Tracking the work needed to migrate from Minima to al-folio. Old site content is in `old_site/`.

---

## Setup & Infrastructure

- [x] Fork al-folio template
- [x] Configure Docker for local dev on port 4000
- [x] Exclude `old_site/` from Jekyll build
- [x] Remove `jekyll-terser` (unavailable on rubygems)
- [ ] Configure GitHub Actions for deployment (needed for `jekyll-scholar` on GitHub Pages)
- [ ] Update CNAME / verify custom domain still works after deploy

---

## Configuration (`_config.yml`)

- [ ] Update name, email, description/bio
- [ ] Update institution and affiliation info
- [ ] Update social links (GitHub, LinkedIn, Google Scholar, Instagram, StackOverflow)
- [ ] Disable/remove features not being used (books, teachings, blog subscriptions, etc.)
- [ ] Set correct URL and baseurl

---

## Content

### Homepage / Bio (`_pages/about.md`)
- [ ] Write short bio paragraph
- [ ] Add profile photo to `assets/img/`
- [ ] Add news items to `_news/` (optional — recent papers, talks, etc.)

### Publications (`_bibliography/papers.bib`)
- [ ] Add FZModules paper (SC Workshops '25 / DRBSD)
- [ ] Add IVSparse / VCSC paper (BigData '24)

### Projects (`_projects/`)
- [ ] Create FZModules project card
- [ ] Create IVSparse project card
- [ ] Remove al-folio demo projects

### CV (`_pages/cv.md`)
- [ ] Embed PDF or link to CV (currently `old_site/assets/images/CV_Jan26.pdf`)

### About / Interests (`_pages/about.md` or separate page)
- [ ] Add hobbies section (hiking, skiing, caves, cooking, mixology, etc.)
- [ ] Migrate photos from `old_site/assets/images/`

### Blog / Posts (`_posts/`)
- [ ] Migrate hello-world post
- [ ] Decide on posting workflow for thoughts/demos

---

## Cleanup

- [ ] Remove al-folio demo content (blog posts, demo projects, placeholder bib entries)
- [ ] Remove unused pages (books, teachings, dropdown demo)
- [ ] Audit and trim `_config.yml` feature flags
- [ ] Delete `old_site/` once migration is complete
