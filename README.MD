# Time of Destruction

A scroll-driven web page for *Time of Destruction*, the personal chapter (pp. 44–55) of **Sketches of Octagon Studio** by Juned Widi Nugroho.

Each drawing gets its own screen: the sheet develops as you scroll, then its quote surfaces word by word. Animation uses GSAP + ScrollTrigger, bundled in `vendor/` so the site has no CDN dependency. Visitors can switch motion off with the button in the bottom-left corner.

## Structure

```
index.html      the whole page (HTML, CSS, JS)
img/            drawings (JPG) and the astronaut cut-out (PNG)
vendor/         gsap.min.js, ScrollTrigger.min.js (3.12.5)
vercel.json     clean URLs + long cache for img/ and vendor/
```

## Deploy

Static site, no build step. On Vercel: import this repo, Framework Preset **Other**, leave build and output settings empty.

Local preview: `npx serve .`
