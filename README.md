# Class Project Template

A collaborative, multi-author website template for course-based digital projects — built on the [Xanthan](https://github.com/xanthan-web/xanthan) framework, hosted on GitHub Pages.

**[Live demo](https://xanthan-web.github.io/class-project-template)** · **[Xanthan docs](https://xanthan-web.github.io/xanthan/docs/)**

---

## What This Is

This template is designed for instructors running collaborative digital humanities, public history, or research projects where students each contribute an essay or artifact to a shared, public-facing site.

The model: one repository, one instructor-managed homepage, many student-authored essay subfolders. The homepage auto-generates a card grid from whatever essay pages exist — no manual linking required as students add their work throughout the semester.

A finished example: [UNM Campus History](https://amaranth.unm.edu/campus-history/)

---

## Structure

```
essays/
  student-project-name/
    index.md        ← student's essay (any layout)
    images/         ← essay-specific images
index.md            ← auto-generated card grid from essays/
about.md            ← course/project description
instructions.md     ← onboarding guide for student contributors
docs/               ← full Xanthan documentation (synced from framework)
```

The homepage card grid is driven by a Liquid query over all pages under `essays/` — no config changes needed as projects are added:

```liquid
{% assign cards = site.pages | where_exp: "p", "p.path contains 'essays/'" %}
{% include nav/card-grid.html cards=cards %}
```

Card content (title, thumbnail, summary) comes from each essay's front matter.

---

## Included Sample Essays

Three AI-generated placeholder essays on Southwest food history demonstrate the full range of Xanthan components:

- Standard essay layout with images and pullquotes
- ScrollStory layout with fixed background images and scroll-driven text boxes
- Figures, carousels, and caption formatting

These are meant to be replaced by real student work. They're useful as structural references while you're setting up.

---

## Student Onboarding

`instructions.md` is a step-by-step guide for students who have never used GitHub or edited Markdown. It covers:

- Opening the GitHub web editor (`.` key shortcut)
- Creating their essay subfolder under `essays/`
- Front matter requirements for the card grid to pick up their work
- Adding images

Once students are oriented, the instructions page can be removed from the nav or deleted.

---

## Getting Started

1. Click **"Use this template"** on GitHub to create your own repository
2. Enable GitHub Pages in your repo settings (source: GitHub Actions)
3. Edit `index.md` and `about.md` for your course
4. Update `_data/nav-top.yml` if you want to adjust navigation
5. Update `_config.yml` (at minimum, set `title` and `baseurl`)
6. Direct students to `instructions.md` for their setup steps

---

## Relationship to Xanthan

This template is one of three maintained distributions of the Xanthan framework:

| Template | Purpose |
|---|---|
| [Portfolio](https://github.com/xanthan-web/portfolio-template) | Single-author personal/academic site |
| **Class Project** | Multi-author collaborative course site |
| [ScrollStory](https://github.com/xanthan-web/scrollstory-template) | Single immersive scrolling narrative |

Framework updates (components, layouts, CSS, docs) are synced from the main [xanthan](https://github.com/xanthan-web/xanthan) repository via GitHub Actions. `XANTHAN_CHANGELOG.md` tracks what changed with each sync. Template-specific files (`_config.yml`, nav data, content pages) are not overwritten by syncs.

All Xanthan components are available in this template — the full component library is documented in `docs/reference/component-library`.

---

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Or with Docker:

```bash
docker-compose up
```

Site serves at `http://localhost:4000`.

