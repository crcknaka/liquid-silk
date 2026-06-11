# Liquid Silk · Nine Scenes

An interactive WebGL gallery of nine pointer-reactive scenes — tuned for the Apple trackpad. Single file, zero dependencies, no build step.

## Run it

- **Easiest:** download `index.html` from the [latest release](../../releases/latest) and open it in any modern browser. That's it.
- Or clone the repo and open `index.html`.
- Or serve it locally: `python3 -m http.server` and open `http://localhost:8000`.

## The scenes

Press **1–9** (or click the rail on the left) to switch.

| # | Scene | What it is |
|---|---|---|
| 1 | **Liquid Silk** | Flowing ink-and-gold silk that swirls into a vortex around the cursor |
| 2 | **Molten Aurum** | Liquid gold with real specular lighting — the light source is your cursor |
| 3 | **Velvet Nebula** | Parallax gas layers, twinkling stars and a gravitational lens at the pointer |
| 4 | **Crystal Prism** | Faceted-glass kaleidoscope with chromatic dispersion along shard edges |
| 5 | **Smoke Noir** | Film-noir smoke with ray-marched volumetric light shafts from the cursor |
| 6 | **Obsidian Bloom** | Glossy magnetic black liquid that spikes and blooms under the pointer |
| 7 | **Opal Mirage** | Mother-of-pearl thin-film iridescence with heat shimmer around the cursor |
| 8 | **Solar Eclipse** | Black disc, blazing corona and lensing — the corona reaches toward your mouse |
| 9 | **Stellar Dust** | 3 000 physics particles: attraction, swirl, shockwaves, ember-like glow |

## Controls

| Gesture | Effect |
|---|---|
| `1–9` | Switch scenes (with a dip-to-black crossfade) |
| Move the mouse | Every scene reacts: swirls, light, lensing, particle stirring |
| Two-finger scroll ↕ | Shifts the color palette |
| Two-finger scroll ↔ | Rotates the flow / swirl direction |
| Pinch | Smooth zoom (Safari gestures + ctrl-wheel in Chrome/Firefox) |
| Click | Shockwave ripple (pushes particles too) |
| Double click | Triple-ring burst + palette kick |

## Details

- Pure WebGL 1, nine fragment-shader scenes sharing one input pipeline (pointer trail, ripples, hue/flow/zoom).
- Scene 9 runs a CPU particle simulation (velocity integration, swirl forces, ripple impulses) rendered as additive point sprites.
- Custom cursor (dot + lagging ring, difference blend), scene rail, hero titles per scene, film grain, vignette, filmic tone curve.
- Calms down when idle, respects `prefers-reduced-motion`, DPR capped at 2 for smooth Retina rendering.

---

Created by [SitesPro](https://sitespro.org)
