# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Single-page static website for **Beaulieu, Huet CPA inc.**, an accounting firm. Plain HTML + CSS: there is no build step, package manager, framework, JavaScript, linter or test suite. To preview, open `index.html` directly in a browser.

All site content and code comments are in **French (fr-CA)**. Keep new content, class names and comments in French to match.

## Files

- `index.html`: the whole site, laid out as a full-screen pale grey page with one centered column (`main.page`, max 42rem). It contains the logo, a button linking to the client portal (CCH iFirm), the services list (a title and a description for each), and a "Nous joindre" section with the general email and both partners' contact cards.
- `style.css`: all styling. Colours are CSS custom properties in `:root`, taken from the logo (marine `#003673`, bleu `#00428c`, gris `#8b8d96`). Use these variables; don't hard-code new colours. A single breakpoint (`max-width: 38rem`) stacks the partner contacts into one column.
- `infos.txt`: the source content the client supplied (portal URL, contacts, services). Check it when editing site content. The page cleans up its wording slightly (punctuation, "etc.", "Impôts des sociétés et **des** particuliers").
- `images/logo.png` is the optimized logo the page uses. It relies on `mix-blend-mode: multiply` to blend its white background into the page. `images/monogramme.png` is the favicon. The root `Logo.png` is the larger original source file and isn't referenced by the page.

## Conventions

- Inline SVG icons (lock, envelope) use `stroke="currentColor"` and `aria-hidden="true"`.
- Phone links use the `tel:+1…` format, and the displayed number uses `&nbsp;` between groups.
- Sections are labelled with `aria-labelledby` pointing to their `h2`.
