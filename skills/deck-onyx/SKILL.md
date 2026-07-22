---
name: deck-onyx
description: Build an "onyx" style HTML slide deck — cinematic near-black keynote with a glacier-blue accent (retheme-able; champagne alternate), one idea per slide, giant stat beats. Jobs-style presenter deck. Use when the user wants an onyx deck, a keynote/cinematic presentation, or a minimal one-idea-per-slide deck on any topic.
---

# Onyx deck

Produce a single self-contained HTML file: a 1600x900 cinematic keynote in the visual system of `template.html` (in this skill's folder). This is a presenter-driven deck — the slides are billboards (readable in 3 seconds); the speaker carries the detail.

## Process

1. **Read `template.html` in this skill's directory first.** Copy its `<style>` and `<script>` blocks essentially verbatim; write new slide markup.
2. **Distill the user's content to 14–20 single ideas.** Each slide is ONE claim, stat, or imperative. If a slide needs a second sentence to be understood, the sub line gets it — never the headline. Find 2–3 numbers in the content worth a giant-stat slide; they are the emotional beats, spaced through the deck (roughly 1/4, 1/2, 3/4).
3. **Write the deck**, then **verify with screenshots** and fix before declaring done.

## Design tokens (do not improvise)

- Background `#0d0e10`, text `#f2f0ec`, dim `#9d9a94`, faint `#4d4c49`, accent `var(--brass)` (default glacier blue `#7ab8ff`; accent `#d3b277` alternate).
- Font: `-apple-system,BlinkMacSystemFont,"Helvetica Neue",...` — the system sans.
- All slides center-aligned flex columns, padding `80px 160px`.
- Type scale: kicker 13px uppercase `.42em` tracking (title slide only) · h1 84px weight 600 `-.02em` · sub 21px dim, max-width 760px · giant stat 300px accent with unit at `.5em` · giant-label 22px dim.
- A 56x2px accent rule sits above every headline except the title slide.
- Slide counter `NN — NN` centered at bottom, barely visible (#373633).

## Slide grammar

- **Statement slide:** rule → h1 (≤ 8 words, may contain one accent `<span class="a">` phrase) → sub (≤ 25 words). Most slides are this.
- **Giant-stat slide:** 300px accent number → one-line label. No headline.
- **Triptych slide** (max 1–2 per deck): rule → h1 → three text columns with accent `01/02/03` numerals, hairline separators, left-aligned.
- **Flow slide:** h1 → inline `a → b → c` sequence, key terms bright, connectors faint.
- Title: kicker → two-line h1 → one-line sub. Close: rule → h1 with accent phrase, nothing else.
- **Directional/compound stats** ("rose 20%, then fell below baseline"): giant number = the single most striking figure; the movement and nuance live entirely in the label line. If no single number dominates, use a statement slide instead.
- **Lists of 4+ items** (there are no bullets in this style): either compress to the three that matter for a triptych, or fold the whole list into one statement slide's sub as a comma-run ("secrets in prompts, hallucinated dependencies, rubber-stamp reviews…"). Never add a fourth column.

## Ruthless checklist

- If a headline wraps to 3 lines, cut words until it doesn't. Subs must not wrap with a one-word orphan — rephrase or adjust max-width.
- Champagne is scarce: one accent phrase OR one stat per slide, never both.
- No bullets, no cards, no boxes, no tables — this style has none.
- Numerals in triptychs at 15px+; nothing that reads as a stray mark.

## Verify (mandatory)

Screenshot at least 5 slides (title, two statements, one giant stat, the triptych, the close):
`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --window-size=1600,900 --screenshot=<out.png> "file://<deck>#N"`
Read each PNG. Check: one idea per slide, 3-second readability, headline balance (no orphan words), stat slides feel like beats. Iterate until immaculate.

## Theming

The palette is the `:root` variable block at the top of the file — retheming is editing those hex values only (the template marks alternates in comments). Honor any palette the user requests; keep contrast: accents must read on their background, and dark-slide support colors should be tinted toward the new accent or neutral gray.
