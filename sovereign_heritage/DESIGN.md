```markdown
# Design System Document: Teraju IP Sdn Bhd

## 1. Overview & Creative North Star: "The Intellectual Atelier"
This design system moves away from the cold, industrial aesthetic of traditional legal tech. Our Creative North Star is **"The Intellectual Atelier."** We treat Intellectual Property not as a dry legal filing, but as a prestigious craft. 

The system utilizes "High-End Editorial" layouts characterized by intentional asymmetry, generous white space, and a tension between the authoritative, literary weight of serif typography (`newsreader`) and the precision of modern sans-serif (`inter`). We avoid the "template" look by layering surfaces like fine stationery, creating a digital experience that feels bespoke, curated, and profoundly stable.

---

## 2. Colors: Depth & Narrative
Our palette reflects the duality of IP: the deep, fertile ground of innovation (Greens) and the steady, unwavering protection of law (Blues).

### The "No-Line" Rule
To achieve a premium editorial feel, **1px solid borders for sectioning are strictly prohibited.** Boundaries are defined through:
- **Tonal Shifts:** Placing a `surface_container_low` section directly against a `surface` background.
- **Negative Space:** Using the spacing scale to create "invisible" gutters that guide the eye.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of materials. 
- **Base Layer:** `surface` (#f8f9ff) for the main canvas.
- **Structural Sections:** Use `surface_container` or `surface_container_low` to define large content blocks.
- **Interactive Elements:** Use `surface_container_lowest` (#ffffff) for cards to make them "pop" against the slightly darker background tiers.

### The "Glass & Gradient" Rule
For floating navigation or high-priority modals, utilize **Glassmorphism**. Apply `surface_variant` at 60% opacity with a 20px backdrop-blur. 
*Signature Polish:* Use a subtle linear gradient from `primary` (#00302c) to `primary_container` (#0d4842) for hero sections to provide a sense of "visual soul" that flat colors cannot replicate.

---

## 3. Typography: The Authoritative Voice
We pair a high-contrast serif with a functional sans-serif to balance "Expertise" with "Modernity."

| Role | Token | Font | Size | Character |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | Newsreader | 3.5rem | High-impact, editorial storytelling. |
| **Headline** | `headline-md` | Newsreader | 1.75rem | Authoritative, scholarly section headers. |
| **Title** | `title-lg` | Inter | 1.375rem | Semi-bold. Direct and professional. |
| **Body** | `body-lg` | Inter | 1rem | Highly legible, default for all long-form text. |
| **Label** | `label-md` | Inter | 0.75rem | All-caps with 0.05rem tracking for metadata. |

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often a crutch for poor layout. In this system, we prioritize **Tonal Layering.**

*   **The Layering Principle:** Place a `surface_container_lowest` (Pure White) card on a `surface_container_low` background. The subtle 2-3% difference in luminance creates a natural "lift" without visual noise.
*   **Ambient Shadows:** If an element must float (e.g., a dropdown), use an extra-diffused shadow: `box-shadow: 0 12px 32px rgba(23, 28, 34, 0.06);`. The shadow color is a tint of `on_surface`, not a generic grey.
*   **The "Ghost Border":** For internal component logic (like input fields), use the `outline_variant` token at 20% opacity. It should be felt, not seen.

---

## 5. Components: Precision & Prestige

### Buttons
*   **Primary:** Background: `primary` (#00302c); Text: `on_primary`. Roundedness: `md` (0.375rem). For hero CTAs, use a subtle gradient to `primary_container`.
*   **Secondary:** Background: `tertiary_fixed_dim` (#e9c176) to represent the "Gold" accent. Use this for "Apply Now" or "Protect My IP" to draw the eye.
*   **Tertiary:** No background. Text: `primary`. For "Cancel" or "Back."

### Cards & Comparison Tables
*   **Cards:** Forbid divider lines. Group content using `title-md` and `body-sm` hierarchy. Use `xl` (0.75rem) padding for breathability.
*   **Comparison Tables:** Avoid zebra-striping with high contrast. Use `surface_container_low` for the header row and `surface_container_lowest` for the body. Use vertical spacing instead of horizontal lines to separate rows.

### Professional Profile Sections
For IP Attorneys and Agents, use asymmetrical layouts. Place a large-scale portrait on one side with an `outline_variant` "Ghost Border" frame, and the `newsreader` headline overlapping the image slightly to create depth.

### Intellectual Property Status Chips
*   **Pending:** `tertiary_container` with `on_tertiary_fixed_variant` text.
*   **Registered:** `primary_fixed` with `on_primary_fixed_variant` text.

---

## 6. Do’s and Don’ts

### Do
*   **Do use "Optical Centering":** In hero sections, align text slightly above the true center to create a more balanced, "lofty" feel.
*   **Do leverage Teraju's Gold:** Use `tertiary_fixed` (#ffdea5) sparingly for small accents (icons, bullet points, or underline flourishes) to signify premium service.
*   **Do prioritize White Space:** If a section feels crowded, double the padding before adding a border.

### Don't
*   **Don't use pure black:** Use `on_surface` (#171c22) for all text to maintain a sophisticated, soft-contrast look.
*   **Don't use standard icons:** Avoid thin-line "wire" icons. Use solid, duotone icons that utilize `primary` and `secondary` colors.
*   **Don't use 100% opaque dividers:** If a separation is required in a list, use a 10% opacity `outline_variant` line that fades out at the edges.

---

## 7. Spacing & Roundedness
*   **Radius:** The "Signature" corner is `md` (0.375rem) for UI elements like buttons and inputs, and `xl` (0.75rem) for large containers. This creates a balance between "Sharp/Expert" and "Modern/Approachable."
*   **Spacing Scale:** Always use 8px increments. For editorial layouts, use 80px, 120px, or 160px for section margins to allow the brand to "breathe."```