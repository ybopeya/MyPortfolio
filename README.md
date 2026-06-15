# Yohali Bopeya — Portfolio
 
A personal portfolio and blog, designed and built from scratch. One single-page
site that moves from an animated intro through my background, skills, experience,
projects, and writing.
 
**Live site:** https://yohali.dev
 
---
 
## Features
 
- **Single-page layout** — every section (home, about, experience, projects, blog)
  lives on one page; the sidebar links smooth-scroll between them.
- **Animated intro** — a typing effect on the hero, powered by Typed.js.
- **Active-section nav** — the sidebar highlights whichever section you're viewing,
  using an `IntersectionObserver`.
- **Reveal-on-scroll** — sections fade in as you reach them (and respect
  `prefers-reduced-motion`).
- **Interactive experience cards** — hover reveals a dashed offset border and a
  background photo for each role.
- **Substack-connected blog** — post cards are rendered from a small list in the
  page, each linking out to the full essay on Substack.
- **Responsive** — works from desktop down to mobile, with hover effects limited to
  pointer devices so nothing sticks on touchscreens.
## Built with
 
- HTML5
- CSS3 (custom properties, Flexbox, Grid)
- Vanilla JavaScript (no framework)
- [Typed.js](https://github.com/mattboldt/typed.js/) — hero typing animation
- Google Fonts — [Ramaraja](https://fonts.google.com/specimen/Ramaraja) (display)
  and [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (body)
## Project structure
 
```
.
├── index.html          # the entire single-page site
├── css/
│   └── style.css       # all styles, organized into labeled sections
└── assets/
    ├── imgs/           # hero gif + experience card photos
    └── icons/          # social icons (linkedin, github, email)
```
 
## Editing

No build step. Open `index.html` in a browser to preview changes, then push to
redeploy.

## Customizing
 
**Colors** — the whole palette is defined as CSS variables at the top of
`css/style.css` under `:root`. Change `--ink`, `--surface`, `--bg`, and
`--ink-strong` to re-theme the entire site at once.
 
**Blog posts** — posts are a list near the bottom of `index.html`. Add an essay by
adding one object; it renders into a card automatically:
 
```js
const SUBSTACK_URL = "https://YOURNAME.substack.com";
const posts = [
  {
    title: "Post title",
    date:  "Jan 2026",
    blurb: "A sentence or two that makes someone want to click through.",
    url:   SUBSTACK_URL + "/p/post-slug"
  },
  // add more here
];
```

**Experience cards** — each card sets its hover photo inline:
 
```html
<div class="card" style="--card-bg:url('assets/imgs/syf.png')">
```
 
Swap the role, company, and image path to add.
 
 
## Contact
 
- LinkedIn — [in/ybopeya](https://linkedin.com/in/ybopeya)
- GitHub — [@ybopeya](https://github.com/ybopeya)
- Email — ybopeya2@illinois.edu
---
 
© 2026 Yohali Bopeya. All rights reserved.
 
