---
name: contentflow-design
description: Use this skill to generate well-branded interfaces and assets for ContentFlow (proyecto académico GPI 2025-26 — gestión web para autónomos creadores de contenido), either for production or throwaway prototypes/mocks/etc. Contains essential design guidelines, colors, type, fonts, assets, and UI kit components for prototyping in Spanish.
user-invocable: true
---

Read the README.md file within this skill first, and explore the other available files (`colors_and_type.css`, `slides/`, `ui_kit/`, `assets/`, `source/planning_full.txt`).

If creating visual artifacts (slides, mockups, throwaway prototypes), copy assets out of `assets/`, link `colors_and_type.css`, and create static HTML files for the user to view. Reuse existing slide layouts in `slides/` as templates — do not redesign from scratch.

If working on production code, copy the CSS variables out of `colors_and_type.css` and read the rules in README.md to become an expert in designing with this brand.

If the user invokes this skill without any other guidance, ask them what they want to build or design (probably more slides for the GPI 2025-26 presentation, or app mockups). Ask short, focused questions in **Spanish (Spain)** since the project is in that language. Then act as an expert designer who outputs HTML artifacts or production code, depending on the need.

**Hard rules for this brand:**
- Spanish (Spain), academic-professional register. No emoji ever. No purple/blue gradients.
- Three fonts only: Bricolage Grotesque (display), DM Sans (body), JetBrains Mono (code/IDs).
- Coral (#F25C3F) is the only accent. Ink (#0F1729) is the only dark. Cream (#FAF6F0) is the only light.
- Slides are 1920×1080. Use `deck_stage.js` for any new deck.
- Iconography: Lucide only.
