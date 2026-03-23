# Design System Strategy: Nocturnal Artistry

## 1. Overview & Creative North Star
**The Creative North Star: "The Midnight Atelier"**

This design system rejects the sterile, flat nature of standard e-commerce. It is built to evoke the quiet, tactile intimacy of crocheting by candlelight. We are moving away from "web-app" utility and toward a "digital editorial" experience. 

To break the "template" look, designers must embrace **Intentional Asymmetry**. Hero sections should not be perfectly centered; instead, use the Spacing Scale to offset high-end product photography against oversized, elegant serif typography. Overlap elements—let a "floating" glass card partially obscure a background image to create a sense of physical depth and curated layering.

## 2. Color & Tonal Depth
The palette is a study in shadow and soft light. We avoid "pure black" in favor of deep, charcoal-based violets to maintain a sophisticated warmth.

*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Structural boundaries must be defined solely through background shifts. For example, a `surface-container-low` section should sit directly against a `surface` background to create a soft, natural break.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers of heavy, matte paper.
    *   **Base:** `surface` (#16121b)
    *   **Nested Content:** Use `surface-container-low` (#1e1a23) for large sections.
    *   **Interactive Cards:** Use `surface-container-high` (#2d2832) to bring items toward the user.
*   **The "Glass & Gradient" Rule:** To evoke the "artisanal tactile" feel, use Glassmorphism for floating navigation or quick-buy overlays. Apply `surface-container-highest` at 60% opacity with a 20px backdrop blur.
*   **Signature Textures:** For primary CTAs, do not use flat fills. Use a subtle linear gradient from `primary` (#d3bdf4) to `primary-container` (#33224e) at a 135-degree angle to give buttons a "silken thread" luster.

## 3. Typography
The typography system balances the heritage of the craft with modern readability.

*   **The Display & Headline (Noto Serif):** These are your "Editorial Voices." Use `display-lg` for evocative brand moments. Letter spacing should be slightly tightened (-0.02em) to feel premium and intentional.
*   **The Body & Labels (Manrope):** This is your "Functional Voice." Manrope’s geometric but soft terminals provide a clean contrast to the ornate serif.
*   **Hierarchy as Identity:** Always pair a `headline-sm` (Serif) with a `label-md` (Sans-serif, All-caps, tracked out to +0.1em) to create a high-end boutique aesthetic.

## 4. Elevation & Depth
In a dark-themed system, shadows must be handled with extreme restraint to avoid a "muddy" appearance.

*   **The Layering Principle:** Use the Tonal Scale for elevation. A "raised" card is simply a shift from `surface-container` to `surface-container-highest`.
*   **Ambient Shadows:** If a floating element (like a modal) requires a shadow, use a 40px blur with 8% opacity. The shadow color must be a tinted violet (#0a080c) rather than neutral gray to maintain the nocturnal atmosphere.
*   **The "Ghost Border" Fallback:** For accessibility in form fields, use the `outline-variant` (#49454c) at **20% opacity**. It should be felt, not seen.
*   **Glassmorphism:** Use for persistent elements (e.g., sticky headers). It creates a "frosted glass" effect where the rich plum tones of the background bleed through, softening the interface.

## 5. Components

*   **Buttons:**
    *   **Primary:** Gradient fill (`primary` to `primary-container`), `xl` (1.5rem) rounded corners. 
    *   **Secondary:** Ghost style. No background, `outline` token at 30% opacity, `on-surface` text.
*   **Cards:** Forbid divider lines. Separate product titles from descriptions using `spacing-2` (0.7rem). Use `surface-container-low` for the card body.
*   **Input Fields:** Use `surface-container-highest` for the input track. No bottom border. Label sits in `label-md` style, 0.5rem above the field.
*   **Chips:** Use for material types (e.g., "Alpaca," "Organic Cotton"). Apply `tertiary-container` (#bdac51) with `on-tertiary-container` text for a "muted gold" wax-seal effect.
*   **Tooltips:** High-contrast `inverse-surface` with `inverse-on-surface` text. `sm` roundedness.
*   **Lists:** For product specs, use `spacing-4` for vertical separation. Never use a horizontal rule; use a subtle background tint change on hover.

**Contextual Component: "The Yarn Palette"**
A custom selection component for crochet kits. Use large, circular `full` roundedness swatches that, when selected, glow with a `surface-tint` (#d3bdf4) outer ring.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical margins (e.g., `spacing-16` on the left, `spacing-24` on the right) for hero layouts.
*   **Do** use `tertiary` (muted gold) sparingly as a "heartbeat" color for small icons or price points.
*   **Do** prioritize high-quality, moody photography with deep shadows and soft highlights.

### Don't:
*   **Don't** use 100% white text. Use `on-surface-variant` (#cbc4cd) for body text to reduce eye strain and maintain the "moody" vibe.
*   **Don't** use sharp corners. Everything must feel "soft but premium," adhering to the `md` (0.75rem) to `xl` (1.5rem) roundedness scale.
*   **Don't** use standard "Success" green. Use the `tertiary` gold for positive confirmations to keep the palette artisanal.