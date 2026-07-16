# SITE STATUS — gabrieledangelo.com

_Last updated: 16 July 2026_

## How to use this file in a new chat

Upload or paste this file and write:

> Continue working on gabrieledangelo.com from this status file. Work one file at a time, always provide the complete file when replacing HTML, and do not overwrite approved work without checking the current state.

---

## 1. Project and workflow

- Personal website: **gabrieledangelo.com**
- GitHub repository: **Gabrieledangelo/gabrieledangelo.com**
- Static website developed locally in VS Code and previewed with Live Server.
- Publishing workflow: save files, commit in Source Control, then **Sync Changes**.
- Work **one file at a time**.
- For HTML replacements, always provide the **entire file**, never isolated fragments.
- For very long CSS changes, prefer a complete downloadable `style.css` to avoid chat truncation.
- Do not assume a cropped screenshot shows the entire page.
- Be direct and pragmatic. Admit uncertainties immediately.

---

## 2. Main creative hierarchy

### Gabriele D’Angelo

The website represents Gabriele as a whole:

- music;
- 3D visual art;
- acting;
- film, theatre and other creative projects.

### IMPERFECT

**IMPERFECT is Gabriele’s personal musical artist identity.**

It is not an album title or a playlist.

### Wooden Key

**Wooden Key is a shared band project**, not exclusively Gabriele’s.

Core members to acknowledge:

- Alberto Mazzucchelli, vocals;
- Gabriele D’Angelo, guitars;
- Cosimo Tranchino, bass.

Wooden Key deserves a separate official website and domain. Gabriele believes that a domain may already have been registered, but the exact address still needs to be confirmed.

On `gabrieledangelo.com`, Wooden Key should remain as a concise project entry that eventually links to the band’s official website, rather than becoming a full internal personal-project page.

---

## 3. Current site files

Main files already present:

- `index.html`
- `about.html`
- `projects.html`
- `stories.html`
- `contact.html`
- `style.css`
- `CNAME`

Project detail pages already created:

- `oro-o-mai-piu.html`
- `3d-visual-art.html`

Known assets include:

- `assets/gabriele-hero.jpg`
- `assets/hero-4k.jpg`
- `assets/imperfect-logo.png`
- `assets/projects/pircante.jpg`
- `assets/projects/3d.jpg`
- song covers and MP3 files inside `assets/songs/`

The real Wooden Key and Tales from NOWHere logo asset filenames still need to be confirmed or added.

---

## 4. Approved homepage state

Hero structure uses a background image, not an `<img>` element:

```html
<section class="hero">
  <div class="hero-bg" role="img" aria-label="Gabriele D'Angelo"></div>
  <div class="hero-copy">
    <h1>
      Music, images and stories.<br>
      Different languages, one creative path.
    </h1>
  </div>
</section>
```

Approved hero text:

> Music, images and stories.  
> Different languages, one creative path.

The CSS background is based on:

```css
.hero-bg {
  position: absolute;
  inset: 76px 0 0;
  background: #000 url("assets/hero-4k.jpg") center top / cover no-repeat;
  animation: heroZoom 20s ease-out forwards;
}
```

Do not casually replace this with an `<img>` because that previously damaged the composition.

---

## 5. About page

Current approved layout:

- portrait on the left;
- biography on the right;
- three parallel disciplines below:
  - Music
  - 3D Visual Art
  - Acting
- closing line: **Never too late.**

The numbers `01`, `02`, `03` were removed from the disciplines.

Design rule agreed:

> Use numbered sections only when the numbers represent real phases or a meaningful sequence.

Do not use decorative numbering merely because there are three columns.

---

## 6. Project detail pages

### `oro-o-mai-piu.html`

Existing project detail page with:

- image of the creature;
- project introduction;
- numbered sections retained because they describe a process or progression;
- current status: **In development**.

Check that its back link points to the correct Projects/Home anchor before final publication.

### `3d-visual-art.html`

Existing project detail page with:

- architectural visualization image;
- text sections:
  - The image
  - The approach
  - 3D practice
- decorative numbers removed because these are parallel aspects, not sequential phases.

---

## 7. Current Projects page

`projects.html` has been redesigned as a compact editorial index rather than a long page containing every article in full.

The cards were reduced by roughly 50% vertically using an override block appended at the bottom of `style.css`.

Current visible order in the latest screenshot:

1. **IMPERFECT**
2. **Wooden Key**
3. **Oro o mai più**
4. **Tales from NOWHere**

Current concept:

- compact horizontal rows;
- image or logo on the left;
- category and status at the top right;
- title, short introduction and link/status text;
- full articles or official sites open separately.

Current entries:

### IMPERFECT

- Category: Music · Solo artist identity
- Status: Ongoing
- Current text link: **Project page coming soon**
- Personal project belonging fully to Gabriele.

### Wooden Key

- Category: Music · Band project
- Status: Current
- Current text link: **Official website coming soon**
- Shared project with Alberto Mazzucchelli and Cosimo Tranchino.
- Must eventually link to the separate official Wooden Key domain.

### Oro o mai più

- Category: Short film
- Status: In development
- Link: **Discover the project →**
- Leads to `oro-o-mai-piu.html`.

### Tales from NOWHere

- Category: Musical · Theatre
- Status: In development
- Current text link: **Project page coming soon**

The latest screenshot does not show 3D Visual Art inside this Projects index. Its existing detail page remains available elsewhere in the website structure.

---

## 8. Projects page visual work still pending

These were the last explicitly discussed adjustments and must not be forgotten:

### IMPERFECT image

The current IMPERFECT visual contains a smaller black rectangle inside the left panel.

Required change:

- enlarge or crop the IMPERFECT artwork so that its black background reaches and visually merges with the edges of the image panel;
- avoid the appearance of a framed image floating inside another black rectangle;
- preserve the logo proportions and readability.

### Wooden Key

The current left panel uses a temporary text recreation reading “WOODEN KEY”.

Required change:

- replace the temporary typographic reconstruction with the **real Wooden Key logo image**;
- keep the compact-row proportions;
- avoid recreating the logo with HTML text once the real asset is available.

### Tales from NOWHere

The current left panel uses a temporary text reconstruction.

Required change:

- replace it with the **real Tales from NOWHere logo image**;
- preserve its specific capitalization: **Tales from NOWHere**.

### Wooden Key domain

Still to determine:

- exact registered domain;
- whether it is active;
- where it is registered;
- whether the Projects card should already open it or temporarily remain non-clickable.

---

## 9. CSS note

A compact override was appended at the end of `style.css`, inside:

```css
/* PROJECTS - COMPACT ROWS */

@media (min-width: 951px) {
  ...
}
```

This override:

- reduces card height to about `175px`;
- reduces internal padding;
- limits descriptions to two lines;
- reduces title and logo size;
- keeps the full width of the cards.

Do not remove it unless deliberately redesigning the Projects index.

Because the compact block is at the bottom of the stylesheet, its rules override earlier Projects Journal rules.

---

## 10. Next session: exact starting point

Begin by doing these steps in order:

1. Inspect the latest actual `projects.html` and the final section of `style.css`.
2. Obtain or identify the real logo files for:
   - Wooden Key;
   - Tales from NOWHere.
3. Fix the IMPERFECT image so its black background reaches the panel edges.
4. Replace both temporary text logos with their real image assets.
5. Confirm the Wooden Key official domain.
6. Change the Wooden Key card from “Official website coming soon” to a real external link only after the domain is confirmed.
7. Preview in Live Server before publishing.
8. Commit and sync only after visual approval.

Suggested future Git commit message:

```text
Refine projects index and add official project branding
```

---

## 11. Current Git checkpoint

Before starting a new chat, save and publish the current state with a checkpoint commit.

Suggested commit message:

```text
Save current site and compact projects journal
```

This checkpoint should include every currently changed HTML file, `style.css`, and any newly added project assets.
