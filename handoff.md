handoff_content = """# Style Handoff: Design Guidelines & Implementation Rules

Follow these numbered design instructions every time you build, style, or edit pages for this project:

1. **Aesthetic & Tone:**
   - Maintain a calm, organic, minimalist digital lifestyle aesthetic (inspired by Nami Matcha and modern Apple product interfaces).
   - The interface must prioritize whitespace, understated refinement, and high legibility.

2. **Color Palette:**
   - **Background:** `#F7F5EF` (Warm cream/oatmeal).
   - **Text / Primary Elements:** `#1E1E1E` (Soft off-black/deep charcoal for high readability without harsh contrast).
   - **Accent Color:** `#6B8F71` (Muted organic matcha green). Use this for all links, divider borders, index numbers, hover states, and key interactive accents.

3. **Typography System:**
   - **Headings Font:** `DM Sans`, sans-serif (weights: 400 regular, 500 medium).
   - **Body & Metadata Font:** `Inter`, -apple-system, BlinkMacSystemFont, sans-serif (weights: 300 light, 400 regular, 500 medium).
   - **Headings Hierarchy:** Headings must remain restrained and small:
     - `H1`: `2.5rem` (`40px`) on desktop, collapsing to `2.0rem` (`32px`) on mobile viewports. Line height: `1.15`.
     - `H2`: `1.5rem` (`24px`). Line height: `1.3`.
     - `H3`: `1.15rem` (`18.4px`).
     - **Body Text:** `1.0rem` (`16px`), line height `1.6`.
     - **Subtitles & Metadata:** `0.875rem` (`14px`), line height `1.5`.

4. **Hero Image Placement:**
   - Position a full-width hero image banner across the very top of the page (`width: 100%`).
   - Dimensions: `height: 40vh` on laptop/desktop, collapsing to `30vh` on mobile screens.
   - Corners & Shadows: Completely flush, square corners (`border-radius: 0`), zero box shadows, `object-fit: cover`.
   - Motion: Apply a gentle entry fade (`opacity: 0` to `1` over `1.4s` cubic-bezier(0.16, 1, 0.3, 1)).

5. **Identity & Name Placement:**
   - Place the site title / creator name (`Liang Jing Ren`) immediately below the hero image container.
   - Alignment: Left-aligned at the top of the main container, followed by metadata (`A.I. for Designers`, course number, institution, and direct email link).
   - Demarcate this section with a crisp, 1px solid bottom border in the accent color (`#6B8F71`).

6. **Layout & Grid System:**
   - **Container Width:** Max width capped at `1200px` centered with horizontal margin auto.
   - **Desktop Layout (>= 768px):** Two-column layout (`grid-template-columns: 1fr 2fr` or left rail / main content split) separated by a `64px` gap.
   - **Mobile Layout (< 768px):** Collapses smoothly into a single-column layout (`grid-template-columns: 1fr`) with reduced padding (`24px` horizontal padding).
   - **Spacing Base Unit:** Adhere to an 8px spacing scale (`8px`, `16px`, `24px`, `32px`, `40px`, `48px`, `64px`, `80px`).

7. **Work List & Links Styling:**
   - Present all assignment links as clean plain-text list items with square corners (`border-radius: 0`).
   - Each item features a structured horizontal layout: a 2-digit index number (`01`, `02`, etc.), project title, and an arrow indicator (`↗`).
   - Default state: Text color `#6B8F71`, bordered top and bottom with a 1px solid border in `#6B8F71`.
   - **Hover Interaction:** On hover, the fill and text swap places instantly over a `200ms` transition (`background-color: #6B8F71; color: #F7F5EF;`). The arrow translates slightly `translate(2px, -2px)`.

8. **Ambient Motion & Background:**
   - Implement an ambient, moving background via pure CSS (no external video, no external image assets).
   - Structure: Fullscreen fixed gradient shifting smoothly between warm cream (`#F7F5EF`) and soft matcha green tones (`#E5ECE4`).
   - Animation: `subtleColorShift 26s ease-in-out infinite alternate` running across a `300% 300%` background size.

9. **Deliverable Architecture:**
   - The webpage must be fully self-contained inside a single `index.html` file (all styles within `<style>`, all scripts within `<script>`).
   - Fully responsive across desktop, tablet, and mobile with zero horizontal overflow.
"""

with open("handoff.md", "w", encoding="utf-8") as f:
    f.write(handoff_content)

print("handoff.md written successfully.")