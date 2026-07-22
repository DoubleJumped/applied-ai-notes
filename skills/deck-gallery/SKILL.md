---
name: deck-gallery
description: Build a "gallery" style HTML slide deck — paper background, white content cards, monochrome black accent (retheme-able; oxblood alternate), full content density. The professional board-room deck. Use when the user wants a gallery deck, a card-style presentation, or a content-rich professional deck on any topic.
---

# Gallery deck

Produce a single self-contained HTML file: a 1600x900 deck of floating card slides on warm paper, in the visual system of `template.html` (in this skill's folder). This is the content-dense style — real information on every slide, readable without a presenter.

## Process

1. **Read `template.html` in this skill's directory first.** It is the authoritative reference for CSS tokens, components, and the nav/scale JS. Copy its `<style>` and `<script>` blocks essentially verbatim; write new slide markup.
2. **Plan the slide sequence** from the user's content: 12–18 slides. Standard arc: dark title → premise → 2–4 sections of content slides → a dark statement slide as the emotional hinge (~60% through) → closing dark statement. Never two dark slides adjacent except title/close.
3. **Write the deck**, then **verify with screenshots** (step below) and fix everything you find before declaring done.

## Design tokens (do not improvise)

- Palette lives in the `:root` block of the template (default: monochrome — paper `#efefec`, ink `#111`, accent `#111`, black statement slides; oxblood `#7d2332` marked as alternate). Use `var(--accent)` everywhere the accent appears.
- Font: `"Helvetica Neue",Helvetica,Arial,sans-serif` only.
- Slide = rounded card (4px radius) inset 26/30px on the paper, soft double shadow, padding `72px 92px 58px`.
- Type scale: eyebrow 12px uppercase letterspaced accent · h1 60px (74px on dark statements), weight 600, `-.015em` · lede 19px `--sub` · card titles 16px · card body 13.5px · bigline 21px with `<em>` phrases in the accent.
- Footer on every slide: section names in 11px uppercase, current section in bold ink, page `NN / NN` right-aligned.

## Slide grammar

- **Content slides:** eyebrow (`Phase N · Name`) → h1 → optional lede → ONE body block (card grid `g2`–`g5`, three-column `cols` with top-rule columns, hairline table, or report panels) → spacer → bigline takeaway with one accent `<em>` phrase → spacer → footer. The bigline is mandatory — it kills hollow bottoms.
- **Dark statement slides:** dark-bg background (accent-dark or black), spacers centering an xl h1 + lede. Max 3 per deck.
- Tables: 2px ink rule under the header row, hairline rows, `→ human`-style cells in the accent.
- Cards: white on the warm card background, hairline border, accent `01` numerals or uppercase tags.

- **Stat-tile slide** (for 2–3 headline numbers): a `g2`/`g3` grid of `.panel` boxes, each body holding a `.pass`-style big number (48px, weight 600) + a `small` qualifier line + one supporting sentence. Use when the content has stat beats; don't force stats into ordinary cards.

## Ruthless checklist (learned the hard way)

- No hollow middles: if a slide's content block is shallow, deepen the content or enrich the bigline — never leave a dead band between block and footer.
- **Known trap:** a single row of short cards + the two spacers reliably produces a hollow middle. If the grid is one row, the slide ALSO needs a lede and ~4 lines of body per card (or use the stat-tile pattern) — plan for this up front rather than fixing it in the verify pass.
- Numerals/labels must read at final size — no decorative marks that look like stray ticks.
- Title and closing dark slides: vertically center with spacers on both sides of the text block.
- Emphasis `<em>` spans: one per bigline, never two.

## Verify (mandatory)

Screenshot at least 5 slides (title, a card-grid slide, a table slide, the dark hinge, the close):
`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --window-size=1600,900 --screenshot=<out.png> "file://<deck>#N"`
Read each PNG. Fix overflow, dead space, widowed lines, misaligned columns. Iterate until every sampled slide would survive the pickiest designer.

## Theming

The palette is the `:root` variable block at the top of the file — retheming is editing those hex values only (the template marks alternates in comments). Honor any palette the user requests; keep contrast: accents must read on their background, and dark-slide support colors should be tinted toward the new accent or neutral gray.
