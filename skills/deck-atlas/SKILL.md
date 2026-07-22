---
name: deck-atlas
description: Build an "atlas" style HTML presentation — a single spatial canvas (Prezi-like zooming map) where slides are smooth camera moves between stations on a loop or process map. Porcelain background, cobalt accent, GPU-friendly. Use when the user wants an atlas deck, a zooming/spatial presentation, or when the content is a cycle/process/system whose shape IS the message.
---

# Atlas deck

Produce a single self-contained HTML file: one 4000x2250 spatial canvas inside a 1600x900 stage, in the visual system of `template.html` (in this skill's folder). "Slides" are camera moves. The overview — the whole map seen at once — is the first and last step and the reason to use this style: only choose it when the content has a real shape (a loop, a pipeline, a hub-and-spokes).

## Process

1. **Read `template.html` in this skill's directory first.** Copy its CSS, the camera/`apply()` JS, and the transition discipline verbatim; replace the map content and the `steps` array.
2. **Design the map before writing HTML:** a center title/thesis node; 4–8 stations arranged in the content's true shape along an SVG path (ellipse for loops, horizontal spine for pipelines); 3–6 smaller satellite callouts (stats, warnings, quotes) placed near the station they belong to. Sketch coordinates on paper first — stations ~640px wide, satellites ~430px, generous water between nodes.
3. **Author the step sequence:** overview → center → stations in narrative order (satellites framed after their station) → a pull-back half-view → full overview. 12–18 steps.
4. **Write the deck**, then **verify every step with screenshots** and retune cameras until every frame is composed.

## Design tokens (do not improvise)

- Paper `#f2f1ed` with a 56px dot grid (radial-gradient), cards white, ink `#191b1f`, sub `#62656c`, hairline `#e0dfd9`, accent cobalt `#2743e6`.
- Path: 3px hairline `#c8cbe8` under a dashed cobalt line at 55% opacity, small solid arrowheads.
- Stations: white cards, 10px radius, 1px hairline, shadow `0 1px 3px rgba(25,27,31,.07)` — nothing heavier. Cobalt number discs, 34px h2, 16px lead line, 14.5px body, pill chips.
- HUD: a solid pill (paper background, hairline border) bottom-center with the step label and `N / N` — solid so it reads over any canvas content.

## Performance rules (non-negotiable — this is why the style works)

- Camera = `translate3d(tx,ty,0) scale(s)` on the ONE canvas div, `transform-origin:0 0`, transition `.85s cubic-bezier(.45,.05,.2,1)`.
- `will-change:transform` set before each move, removed on `transitionend` (forces re-raster so text is crisp at the new scale).
- First frame SNAPS: disable the transition, apply step, force reflow, re-enable. Never animate in from identity on load.
- No filters, no blurs, no glows, no backdrop-filter, minimal shadows. Zoom scale range roughly 0.4–1.8; camera math: `tx = 800 - cx*s`, `ty = 450 - cy*s`.
- `prefers-reduced-motion` → transition none.

## Ruthless checklist

- Overview must fit the entire map with nothing clipped: at s=0.40 exactly the full 4000x2250 is visible — keep all nodes inside with margin.
- No frame may cut a card mid-glyph or mid-word at the viewport edge. A clean padding-sliver or a deliberate full peek is fine; reposition nodes or retune `{cx,cy,s}` until true.
- Neighboring-node peeks are ZUI grammar (context), but the focused node must be unmistakably framed.
- HUD rule, precisely: content sitting fully BEHIND the solid pill is fine (the pill reads over it); content poking out above or beside the pill mid-frame is a collision — retune the camera.
- A satellite that relates to two stations is framed exactly once, after the first of its stations in narrative order.
- Station text ~14.5px is authored for s≈1.1–1.5 viewing; station titles must remain readable in the overview.

## Verify (mandatory)

Screenshot EVERY step (they're cheap and cameras are fiddly):
`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --window-size=1600,900 --screenshot=<out.png> "file://<deck>#N"`
Read each PNG. Check framing, clipping, HUD collisions, overview completeness. Retune coordinates/cameras and re-shoot until every step is composed like a deliberate photograph.

## Theming

The palette is the `:root` variable block at the top of the file — retheming is editing those hex values only (the template marks alternates in comments). Honor any palette the user requests; keep contrast: accents must read on their background, and dark-slide support colors should be tinted toward the new accent or neutral gray.
