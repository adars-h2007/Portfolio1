# Adarsh Patil — Portfolio

A single-page personal portfolio built with plain **HTML, CSS and JavaScript**. It has a bold black-and-red look and a short intro animation where labelled cursors build the page as it loads. There are no frameworks and no build step.

**Live site:** https://portfolio-hazel-nine-27.vercel.app

## Features

- **Intro animation:** four labelled cursors (*Layout*, *Type*, *Color*, *Code*) click the hero into place on first load. A **Skip intro** button is available, and the intro plays once per browser session.
- **Scroll build:** content below the hero fades in as the cursors "click" each element into place while you scroll. After the intro the cursors keep following your mouse.
- **Replay intro:** a button in the footer replays the animation.
- **Project showcase:** 10 projects with filters (All, React, Java, Python, HTML & CSS) and a live project count.
- **Project details dialog:** click a project to open a modal with its description, tech stack and GitHub link.
- **Scrolling tech marquee** of the tools I use.
- **Results, About and Skills sections**, plus a "Design to deployment" process section and a contact section.
- **Optional hero photo:** add a `photo.png` next to `index.html` and it replaces the code card in the hero.
- **Responsive layout** with a mobile menu, and the current section is highlighted in the nav.
- **Accessibility:** skip link, keyboard-friendly menu (Esc closes it), focus styles, ARIA labels, and a dialog that returns focus when closed.
- **Reduced motion:** the intro, cursors and marquee animation are turned off for visitors who prefer reduced motion. Touch devices skip the cursors.

## Project structure

```
.
├── index.html    # Page markup and the project data (JSON)
├── style.css     # All styles, layout, responsive rules and animations
├── main.js       # Menu, filters, project dialog and the cursor animation
└── photo.png     # Optional: hero photo (transparent PNG)
```

## Run locally

No installation is needed.

```bash
git clone https://github.com/adars-h2007/Portfolio.git
cd Portfolio
```

Open `index.html` in your browser. To serve it locally instead:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Customising

**Add or edit a project**

1. In `index.html`, add a card inside the project list, copying an existing one:
   - `data-tags` holds the filter tags (`react`, `java`, `python`, `html`)
   - `data-id` on the button must match a key in the JSON data block
   - `--h` sets the card's colour tint
2. Add a matching entry to the JSON in `<script id="data" type="application/json">` with `name`, `kind`, `desc`, `stack` and `links` (a list of `["Label", "URL"]` pairs).
3. Update the starting number in `<span id="count">`. The count updates by itself once a filter is clicked.

**Change colours and fonts:** edit the variables at the top of `style.css` (`--red`, `--red-deep`, `--bg`, `--head`, `--body`, `--script`).

**Update text, education and contact details:** edit the matching sections in `index.html`.

**Use a hero photo:** save a transparent `photo.png` next to `index.html`.

## Deploy

The site is static, so it works on any static host.

- **Vercel (current setup):** import the repository and deploy with the default settings. No build command is needed.
- **GitHub Pages:** go to *Settings → Pages*, choose the `main` branch and the root folder, and save.

## Tech used

- HTML5, CSS3 (custom properties, grid, flexbox)
- Vanilla JavaScript (IntersectionObserver, `<dialog>`, sessionStorage)
- Google Fonts: Anton, Outfit, Caveat

## Projects featured on the site

- Recall (interview preparation tracker)
- LiveTrack
- Campus Lost & Found
- Civic Issue Tracker
- Clinic No-Show Reduction System
- Shree Wholesale Billing
- [Appointment Booking Website](https://github.com/adars-h2007/appointment)
- [Body Builder App](https://github.com/adars-h2007/Body-Builder-App)
- [Developer Portfolio](https://github.com/adars-h2007/Portfolio) (this repo)
- [Electronic Shop](https://github.com/adars-h2007/Electronic-Shop)

## Contact

- GitHub: [@adars-h2007](https://github.com/adars-h2007)
- LinkedIn: [Adarsh Patil](https://www.linkedin.com/in/adarsh-patil-587a65319/)
- Email: adarshpatil6650@gmail.com

---

© Adarsh Patil. All rights reserved.
