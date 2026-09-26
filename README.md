# National Developer

Landing page for Development, a residential developer in Kyiv, with GSAP animations on load and on scroll. The site is in Ukrainian. Built in July 2021 as a learning project.

**Live demo:** [androfficial.github.io/html-national-developer](https://androfficial.github.io/html-national-developer/)

## Features

- On load, a GSAP timeline brings in the intro: the title and subtitle rise, the header drops in, the decorative elements scale up, and the round scroll button spins in and then keeps bobbing (CSS keyframes).
- The scroll button smoothly scrolls to the benefits section.
- ScrollTrigger timelines reveal each section as it enters the viewport: benefits, the chief architect's quote, building standards, smart home features, projects and news, with staggered items.
- The smart home icons jump in a repeating wave that pauses while the cursor is over them.
- Sections: three key benefits, a quote, eight building standards, four smart home features, three residential complexes with location, class and status, a news grid, and a footer with the office address, phones and links.

## Tech stack

- **Framework:** none, plain HTML and JavaScript
- **Styling:** SCSS compiled to CSS (the SCSS sources are not in the repository)
- **Animation:** GSAP 3 with ScrollTrigger, CSS keyframes
- **Tooling:** built with Gulp 4, which produced the plain and minified bundles in `css/` and `js/`
- **Hosting:** GitHub Pages

## Getting started

The repository holds the compiled site, with no dependencies and no build step. The icons and logos come from an external SVG sprite that browsers do not load from `file://`, so serve the folder over HTTP, for example with `npx serve .` on Node.js 18 or later.

```bash
git clone https://github.com/androfficial/html-national-developer.git
cd html-national-developer
npx serve .
```

Then open the local address that `serve` prints.

## Notes

- The animations depend on the window width at load time: the intro timeline runs above 1023 px and the scroll animations above 1180 px. Narrower windows show the page without them.
- The burger button in the header has no menu attached, and the "more" links point to `#`.
