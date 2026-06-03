# AI Context

## Project

This repository contains an HTML slide presentation for the paper **"Monetary Dynamics in Dollarized Economies: The Case of Ecuador"** by **Juan Pablo Erraez** and **Juan Lorenzo Maldonado**.

The current deck is a short presentation version for the **IV Congreso Anual Asociacion de Economia del Ecuador**. It points readers to the full paper published in **Cuestiones Economicas, Banco Central del Ecuador, December 2025**, DOI: `https://doi.org/10.47550/RCE/35.2.3`.

## Purpose

The next task is to produce an even shorter version of the current HTML presentation. Future AI agents should preserve the academic argument and the existing visual language while reducing slide count, text density, and repetition.

## Core Argument

The presentation explains monetary dynamics in Ecuador's dollarized economy through a Money View framework:

- Dollarization does not eliminate money creation; it changes the hierarchy and constraints under which money is created.
- Ecuador cannot issue the apex international settlement asset, the US dollar, so high-powered money depends on balance-of-payments flows, borrowing, and institutional balance-sheet mechanics.
- Domestic credit and fiscal operations can create deposits without a matching inflow of "green dollars," generating monetary and balance-of-payments pressures.
- Central bank financing, cross-holdings, and fiscal-monetary links are key risk channels.
- Reserve adequacy should be evaluated with broad international reserves and dynamic flows, not only static official reserve metrics.

## Current Deck Structure

The current `index.html` is a single-file, full-screen HTML slide deck. Use the visible slide counter order as the canonical slide numbering when discussing changes with the user; some internal HTML comments preserve older numbering from previous versions. Main content blocks:

1. Title slide with QR code to the paper.
2. Presentation structure.
3. Money View framework: hierarchy, endogenous money, and the dollarization constraint.
4. Ecuador institutional context: seven features shaping dollar flows.
5. Dual currency and primary money creation.
6. Risk channel 1: central bank financing, with central-bank and commercial-bank balance sheets.
7. Risk channel 2: cross-holdings and illusory liquidity, based on section 3.2.2 of the paper.
8. Risk channel 3: fiscal-monetary link.
9. Open questions: sustainability, BCE role, and reserve adequacy.
10. Conclusions: five key takeaways.
11. Thank-you / closing slide with QR code.

## Design System

The deck is intentionally editorial and academic, not corporate-dashboard style.

Preserve these design choices:

- Single self-contained `index.html` file with embedded CSS and JavaScript.
- Full-screen `.slide` sections using vertical scroll snap.
- Warm paper palette:
  - `--paper: #f5f2ea`
  - `--paper-alt: #ede9de`
  - `--paper-deep: #e4dfd1`
  - `--ink: #1a1814`
  - red accent `#b8202f`
  - secondary green and amber accents.
- Typography:
  - Display: `Playfair Display`
  - Body: `Source Sans 3`
- Large serif titles, restrained body text, red italic emphasis, thin rules, light panels.
- Fixed progress bar and slide counter.
- Reveal animations via `.reveal` and IntersectionObserver.
- Keyboard, wheel, and touch navigation.
- QR codes generated with `qrcodejs`.

## Shortening Guidance

When making the shorter version:

- Keep the title, central argument, three risk channels, and conclusions.
- Compress framework exposition into one slide unless the audience needs the balance-sheet mechanics.
- Merge "Institutional Context" and "Dual Currency / Primary Money Creation" if slide count must fall sharply.
- Preserve at least one concrete visual balance-sheet or flow mechanism; the paper's contribution is mechanical, so the shorter deck should not become only text.
- Prefer fewer slides with clearer visual hierarchy over deleting all detail.
- Avoid adding new design systems, libraries, build tools, or multi-file frameworks unless explicitly requested.
- Avoid generic marketing language. Keep the tone analytical, precise, and suitable for an academic economics audience.

## Editing Notes

- The deck currently uses inline styles in several slides. Match local patterns when editing rather than refactoring the whole file.
- Slides 5, 6, and 7 were recently redesigned with prefixed CSS classes (`s5-`, `s6-`, `s7-`) to avoid disturbing older figure styles.
- Slide 7 should preserve the accounting logic from paper section 3.2.2: Bank A and Bank B cross-hold certificates; system-wide BCE reserves stay at 3,000 while deposits rise from 16,000 to 16,400.
- Do not remove the disclaimer about authors' views.
- Keep author names visible on opening and closing slides.
- Keep the DOI QR code unless specifically asked to remove it.
- Test changes by opening `index.html` directly in a browser and checking desktop and mobile-ish widths.
