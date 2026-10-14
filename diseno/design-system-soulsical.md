# Design System Document

## 1. Overview & Creative North Star: "The Velvet Stage"
This design system is not a utility; it is a performance. We are moving away from the "software as a tool" aesthetic and toward "digital scenography." The Creative North Star is **The Velvet Stage**—an experience that balances the raw, commanding presence of a Broadway lead with the refined, quiet sophistication of a high-end editorial spread.

To break the "template" look, designers must embrace **Intentional Asymmetry**. Do not center-align everything by default. Use "Spotlight Composition," where a large headline (The Star) is offset by a cluster of smaller, utilitarian elements (The Ensemble), leaving vast areas of empty space to represent the darkened theater. We are building an environment that feels intimate, expensive, and deeply emotional.

---

## 2. Colors: Tonal Depth & Spotlight
The palette is built on deep purples and muted greys, designed to mimic the atmosphere of a theater just before the curtain rises.

### Color Tokens
*   **Primary (`#d3bbff` / `#794fc9`):** The "Spotlight." Use for high-intensity actions and accents.
*   **Secondary (`#d3c0df` / `#907f9c`):** The "Gauze." Used for softer, supportive elements.
*   **Surface Hierarchy:** 
    *   `surface`: `#131313` (The Infinite Dark)
    *   `surface-container-lowest`: `#0e0e0e` (The Pit)
    *   `surface-container-high`: `#2a2a2a` (The Stage)

### The "No-Line" Rule
**Explicit Instruction:** Prohibit 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. To separate a hero from a feature section, transition from `surface` to `surface-container-low`. We do not "box" content; we layer it.

### The "Glass & Gradient" Rule
To achieve "Stage Presence," use subtle radial gradients. A hero background should never be a flat hex code. Use a radial gradient centered at the top-left or top-right: `radial-gradient(circle at top, #250059 0%, #131313 70%)`. This mimics the throw of a Fresnel spotlight.

---

## 3. Typography: The Leading Voice
The typography is a duet between the aggressive, condensed power of **Anton** and the rhythmic, modern clarity of **Poppins**.

*   **Display-LG (Anton, 3.5rem):** The "Title Card." Use for hero sections. Always use `letter-spacing: 0.02em` and `text-transform: uppercase`.
*   **Headline-MD (Anton, 1.75rem):** The "Scene Header." Commanding but accessible.
*   **Body-LG (Poppins, 1rem):** The "Narrative." Set with generous `line-height: 1.6` to ensure the editorial feel.
*   **Label-MD (Poppins, 0.75rem):** The "Program Notes." Always use `font-weight: 600` and `letter-spacing: 0.1em` for a premium, metadata-heavy look.

---

## 4. Elevation & Depth: Tonal Layering
We do not use structural lines to create hierarchy. We use "Physicality."

*   **The Layering Principle:** Place a `surface-container-highest` card on top of a `surface` background to create a natural, soft lift.
*   **Ambient Shadows:** For "Floating" elements (Modals, Dropdowns), use a shadow: `box-shadow: 0 20px 40px rgba(0,0,0,0.4)`. The shadow must be large and diffused, never sharp.
*   **Glassmorphism:** For top navigation or floating action bars, use: 
    *   Background: `rgba(32, 32, 31, 0.7)` (surface-container)
    *   Backdrop-filter: `blur(12px)`
    *   This creates the illusion of a frosted stage scrim.
*   **The Ghost Border:** If a form input requires a border, use `outline-variant` at **15% opacity**. Anything higher feels corporate and "cheap."

---

## 5. Components: Expressive Primitives

### Expressive Cards
Cards should not have borders. 
*   **Structure:** Use `surface-container-low`. On hover, transition to `surface-container-high`.
*   **Composition:** Images should use a "Portrait" aspect ratio (3:4) to mimic playbill posters. Typography should bleed off the edges or overlap the image slightly (using negative margins) to break the grid.

### Elegant Forms
Forms are "The Script." They must feel quiet and professional.
*   **Inputs:** No background color. Only a bottom border (1px, `outline-variant` @ 20%). 
*   **Focus State:** The bottom border transforms into a 2px `primary` line, and the label (Poppins) slides up and shrinks. 
*   **Buttons:** 
    *   **Primary:** Anton, all-caps, `primary-container` background. No rounded corners (`0.25rem` max).
    *   **Secondary:** Ghost style. `on-surface` text with a `primary` spotlight glow on hover (box-shadow).

### The Artistic Footer
The footer is the "Final Bow." 
*   Avoid standard columns. Use one massive **Anton** headline of the brand name or a quote, spanning the full width. 
*   Place links in a tight, sophisticated grid at the very bottom, using `label-sm` Poppins. 
*   Use a `surface-container-lowest` background to give the site a grounded, heavy finish.

---

## 6. Do’s and Don'ts

### Do:
*   **Do** use extreme whitespace. If you think there is enough space, add 32px more.
*   **Do** overlap elements. Let a headline sit 20px over an image to create depth.
*   **Do** use "Spotlight Lighting." Use the `primary-fixed-dim` color for subtle glow effects behind key components.

### Don’t:
*   **Don’t** use 100% opaque borders. It kills the theatrical atmosphere.
*   **Don’t** use standard "Success Green" or "Warning Yellow" at full saturation. Use the system's `error` (`#ffb4ab`) and `primary` tokens to keep the palette sophisticated.
*   **Don’t** use center-alignment for long-form text. Keep it left-aligned (Editorial Standard) for a professional look.
*   **Don’t** use generic icons. If icons are needed, use "Thin-stroke" or "Light" variants to match the Poppins weight.