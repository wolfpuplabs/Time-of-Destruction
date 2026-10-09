# Time of Destruction

A scroll-driven web page for *Time of Destruction*, the personal chapter (pp. 44–55) of **Sketches of Octagon Studio** by Juned Widi Nugroho.

Each drawing gets its own screen: the sheet develops as you scroll, then its quote surfaces word by word. Animation uses GSAP + ScrollTrigger, bundled in `vendor/` so the site has no CDN dependency. Sound and animation toggles sit top-right, next to the page counter.

**Sound** (on by default: the opening screen's Begin button is the tap browsers require before audio can play; "Begin without sound" skips it) is generated live with the Web Audio API, no audio files: a binaural bed (110 Hz left, 116 Hz right, a 6 Hz theta beat, best on headphones) under a post-rock score in A (F#m–D–A–E, 66 bpm). Its intensity follows scroll position: delay-guitar arpeggios, then bass, kick and cymbal swells, then tremolo picking near the end, easing off on the last page.

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
