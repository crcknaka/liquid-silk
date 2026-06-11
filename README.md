# Liquid Silk

An interactive WebGL "liquid silk" scene that reacts to your mouse — tuned for the Apple trackpad. Dark ink, teal-and-gold iridescence, a living vortex under the cursor. Single file, zero dependencies, no build step.

## Run it

- **Easiest:** download `index.html` from the [latest release](../../releases/latest) and open it in any modern browser. That's it.
- Or clone the repo and open `index.html`.
- Or serve it locally: `python3 -m http.server` and open `http://localhost:8000`.

## Controls

| Gesture | Effect |
|---|---|
| Move the mouse | The silk swirls around the cursor; a golden trail follows |
| Two-finger scroll ↕ | Shifts the color palette |
| Two-finger scroll ↔ | Rotates the flow direction |
| Pinch | Smooth zoom (Safari gestures + ctrl-wheel in Chrome/Firefox) |
| Click | Shockwave ripple |
| Double click | Triple-ring burst + palette kick |

## Details

- Pure WebGL fragment shader: domain-warped fbm noise, cosine palette, filmic tone curve, grain, vignette, chromatic aberration near the pointer.
- Custom cursor (dot + lagging ring, difference blend), hero parallax, shimmering typography.
- Calms down when idle, respects `prefers-reduced-motion`, DPR capped at 2 for smooth Retina rendering.

---

Created by [SitesPro](https://sitespro.org)
