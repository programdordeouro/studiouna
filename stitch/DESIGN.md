# Design System Strategy: The Tactile Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Ethereal Sanctuary"**

This design system is not a utility; it is an atmosphere. To capture the essence of a luxury nail salon in Indaiatuba, we move away from the rigid, boxy constraints of traditional web apps and toward the fluid, breathing layouts of high-end fashion editorials. 

The goal is to evoke the feeling of a physical space—where light filters through linen and surfaces are soft to the touch. We achieve this through **Intentional Asymmetry**, where images and text blocks overlap to break the "grid-lock," and **Tonal Depth**, where the UI feels layered like fine stationery rather than a flat digital screen. We are building a "Digital Sanctuary" that feels as curated as the service itself.

---

## 2. Color & Surface Philosophy
The palette is rooted in warmth and "skin-tone" neutrals, designed to feel organic and high-end.

- **Primary (`#7f5441`) & Primary Container (`#c9957f`):** Used for Rose Gold accents and core actions.
- **The "No-Line" Rule:** Standard 1px borders are strictly prohibited for sectioning. To separate content, use a background shift from `surface` to `surface-container-low`. Boundaries are felt, not seen.
- **Surface Hierarchy & Nesting:** Treat the UI as a series of physical layers. 
    - Base Layer: `surface` (#fdf8f5)
    - Sub-Sections: `surface-container-low` (#f8f3f0)
    - Interactive Cards: `surface-container-lowest` (#ffffff)
- **The "Glass & Gradient" Rule:** Use Glassmorphism for floating navigation bars or appointment modals. Apply a `backdrop-blur: 12px` and use `surface` at 80% opacity. 
- **Signature Textures:** For Hero CTAs, use a subtle linear gradient from `primary` (#7f5441) to `primary_container` (#c9957f) at a 135-degree angle to mimic the metallic sheen of rose gold.

---

## 3. Typography: Editorial Sophistication
Typography is our primary tool for luxury. We pair the poetic nature of a serif with the modern clarity of a geometric sans.

- **Display & Headline (Cormorant Garamond / Newsreader Scale):** 
    - Use `display-lg` and `headline-md` primarily in *Italic*. This conveys a handwritten, bespoke quality. 
    - *Usage:* Editorial quotes, service categories, and hero statements.
- **Title & Body (Jost / Plus Jakarta Sans Scale):** 
    - Set to "Light" (300 weight) for body copy. The generous letter-spacing and light stroke reflect the "accessible luxury" of the brand.
- **The "High-Contrast" Scale:** To create an editorial feel, keep a wide gap between your heading sizes and body sizes. A `display-lg` title should often be paired with a much smaller, tracked-out `label-md` uppercase sub-header.

---

## 4. Elevation & Depth
Depth in this system is achieved through light and layering, never through heavy shadows.

- **Tonal Layering:** Instead of a shadow, place a `surface-container-lowest` (#ffffff) card on a `surface-container` (#f2edea) background. This creates a "soft lift" that feels natural and premium.
- **Ambient Shadows:** When a floating effect is required (e.g., a "Book Now" FAB), use a custom shadow: 
    - `box-shadow: 0 12px 32px rgba(42, 31, 27, 0.06);` 
    - Note the use of the "on-surface" color (#2a1f1b) at a very low opacity to mimic real-world light.
- **The Ghost Border:** If a form field or container needs a boundary for clarity, use the `outline_variant` (#d5c3bc) at **15% opacity**. It should be a whisper, not a statement.
- **Roundedness:** Use the `xl` (3rem) or `lg` (2rem) tokens for main containers. The "full" (9999px) token is reserved for buttons and chips to maintain a pill-like, organic softness.

---

## 5. Components

### Buttons
- **Primary:** `primary` background with `on_primary` text. Shape: `full` (pill). No shadow.
- **Secondary:** `surface-container-low` background with `primary` text. Use a subtle `outline-variant` ghost border.
- **Tertiary:** Text-only in `primary`, using a `title-sm` font weight.

### Input Fields
- **Styling:** Use `surface-container-lowest` for the field background. 
- **States:** On focus, transition the background to `surface` and apply a 1px ghost border using the `primary_container` color.
- **Error:** Use `error` (#ba1a1a) only for the helper text; the field border should remain subtle to avoid "shouting" at the user.

### Cards & Lists
- **The Divider Rule:** Forbid the use of horizontal lines. To separate list items, use increased vertical padding (from the spacing scale) or a very subtle shift to a `surface-container-high` background on hover.
- **Editorial Cards:** For services, use asymmetrical image-to-text ratios. Let the image bleed over the edge of the card container using a negative margin to create a "collage" effect.

### Selection Chips
- Use the `primary_fixed` (#ffdbcd) color for selected states. The soft blush pink reinforces the "feminine warmth" without the aggression of a high-contrast selection.

---

## 6. Do’s and Don’ts

### Do:
- **Do** use generous whitespace. If you think there is enough room, add 24px more.
- **Do** use "Editorial Offsets." Place a heading so it slightly overlaps an image container.
- **Do** use `Cormorant Garamond Italic` for emphasis words within a sentence of `Jost` body text.

### Don't:
- **Don’t** use black (#000000). Always use `on_surface` (#1c1b1a) or `primary` for text to keep the palette warm.
- **Don’t** use sharp 90-degree corners. Everything must feel "tumbled" and soft.
- **Don’t** use standard "drop shadows" with default offsets. Shadows must be centered and diffused, representing ambient glow, not a direct light source.
- **Don't** use icons that are too heavy. Use "Light" or "Thin" weight iconography to match the `Jost Light` typography.