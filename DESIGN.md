# Design System Strategy: The Gilded Monolith

## 1. Overview & Creative North Star: The Gilded Monolith
The Creative North Star for this design system is **"The Gilded Monolith."** We are moving away from the "flat web" toward a UI that feels like a physical, high-tech artifact—a dark, obsidian-like structure illuminated by precision-engineered light.

To break the "template" look, we utilize **Intentional Asymmetry**. Do not center-align everything. Use the 8.5rem (24) spacing token to create vast "voids" of space, allowing typography to breathe like a luxury editorial magazine. Elements should overlap; a title-lg might break the boundary of a glassmorphism card to create a sense of Z-axis depth and 3D motion.

---

### 2. Colors & Surface Philosophy
The palette is rooted in `surface` (#131313) and `primary` (#f2ca50). This is a high-contrast, high-authority environment.

*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. To separate a hero from a feature section, shift the background from `surface` to `surface-container-low`. Use the `spacing` scale to define boundaries through negative space, not lines.
*   **Surface Hierarchy & Nesting:** Treat the UI as stacked sheets of volcanic glass. 
    *   Base layer: `surface`
    *   Sub-sections: `surface-container-low`
    *   Interactive cards: `surface-container`
    *   Floating modals: `surface-bright`
*   **The "Glass & Gradient" Rule:** To achieve the "3D" vibe, use glassmorphism on floating elements. Use `surface-variant` at 40% opacity with a `backdrop-filter: blur(20px)`. 
*   **Signature Textures:** For primary CTAs, do not use flat gold. Apply a linear gradient from `primary` (#f2ca50) to `primary-container` (#d4af37) at a 135-degree angle to simulate the sheen of brushed metal.

---

### 3. Typography: Editorial Authority
We pair the technical precision of **Inter** with the geometric elegance of **Manrope**.

*   **Display & Headlines (Manrope):** Use `display-lg` (3.5rem) for hero statements. Tighten letter-spacing to -0.02em for a "locked-in" premium feel. This font represents the "Zen" in the brand—balanced and bold.
*   **Body & Labels (Inter):** Inter handles the functional load. Use `body-md` (0.875rem) for general copy. Ensure a line-height of 1.6 to maintain the "luxurious minimalist" aesthetic.
*   **Tonal Contrast:** Use `on-surface-variant` (#d4c5af) for secondary labels to create a sophisticated, muted gold-grey tone that reduces visual noise compared to pure white.

---

### 4. Elevation & Depth: Tonal Layering
In this design system, shadows are not "dark spots"; they are "occlusions of light."

*   **The Layering Principle:** Instead of shadows, use the surface scale. A `surface-container-highest` card sitting on a `surface` background provides all the "lift" required.
*   **Ambient Shadows:** For floating elements (Modals/Dropdowns), use a shadow color derived from `on-primary` at 5% opacity with a 40px blur. It should feel like a soft glow, not a drop shadow.
*   **The "Ghost Border" Fallback:** If a container needs more definition (e.g., inside a busy glassmorphism stack), use the `outline-variant` token at 15% opacity. This creates a "specular edge" rather than a border.
*   **The Glow State:** Interactive elements should utilize a `surface_tint` (#e9c349) outer glow (8px blur, 20% opacity) when hovered to simulate high-tech luminescence.

---

### 5. Components

*   **Glowing Buttons:**
    *   *Primary:* Gradient from `primary` to `primary-container`. `radius-md` (0.375rem). No border. On hover, increase brightness and add a subtle `primary` glow.
    *   *Tertiary:* Ghost style. No background. Use `primary` for text and a "Ghost Border" on hover.
*   **Sleek Cards:** Use `surface-container-low`. Forbid dividers. Separate header from body using a `3.5rem (10)` vertical spacing jump. Use `radius-lg` (0.5rem) for a modern, soft-tech corner.
*   **Glass Chips:** Semi-transparent `secondary-container` backgrounds with `full` (9999px) roundedness. Use `label-md` for text.
*   **Input Fields:** `surface-container-lowest` background. Only a bottom "Ghost Border" using `outline-variant`. On focus, the border transitions to `primary` with a 2px height.
*   **The "Zen" Loader:** A 3D-rotating torus or geometric shape using the `primary` gold gradient, rather than a standard circular spinner.

---

### 6. Do's and Don'ts

*   **DO:** Use asymmetrical padding (e.g., 8.5rem on the left, 4rem on the right) to create a dynamic, custom feel.
*   **DO:** Leverage `surface-container` tiers to create depth.
*   **DON'T:** Use 1px solid white or grey borders. This instantly "cheapens" the premium aesthetic.
*   **DON'T:** Use pure #FFFFFF for long-form text. Use `on-surface` (#e2e2e2) to reduce eye strain and maintain the "dark mode luxury" tone.
*   **DO:** Ensure all glassmorphism effects have a fallback background color for accessibility in environments that do not support backdrop-blur.
*   **DON'T:** Overuse the gold `primary` color. It is a "high-value" accent. If more than 15% of the screen is gold, the "luxury" effect is lost to "gaudiness." Keep it concentrated in CTAs and key brand moments.