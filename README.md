# FutureLabo

![FutureLabo screenshot](docs/screenshots/Future_labo.png)

Single-page interactive SVG + canvas animation.

- The UI is a large inline SVG in `index.html`.
- Animations are driven by GSAP (motion paths, morphs, timelines).
- A transparent `<canvas>` overlay runs Matter.js physics (bubbles + click-to-spawn balls).

## Run

Fastest: open `index.html` in a browser.

If your browser blocks local script/module loading, run a local server instead:

```sh
python3 -m http.server
```

Then open `http://localhost:8000/`.

## Build (webpack)

`dist/main.js` is the generated bundle. Edit source in `src/` and rebuild:

```sh
npm ci
npx webpack
```

## Project structure

- `index.html` — page markup + inline SVG; loads `dist/main.js`
- `src/index.js` — source code for all animations + Matter.js setup
- `dist/` — webpack output (do not edit by hand)
- `css/styles.css` — layout + canvas/button styles
- `pathseg.js` — SVG path segment polyfill used by some browsers

## Notes

- The repo root is not a git repo, but there is a separate git repository inside `git/`.
