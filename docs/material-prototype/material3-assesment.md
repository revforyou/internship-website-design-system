---
hide:
  - toc
---

# Material 3 Evaluation for TWE Design System

## Overview

This document summarizes an evaluation of using **Material&nbsp;3 (M3)** as a baseline for the TWE Design System. The goal was not to replace our components with Google's components, but to see whether **M3 design tokens** (color, typography, shape, elevation) can provide a scalable foundation that we layer our own HTML/SCSS components on top of.

The prototype lives under:

- `docs/material-prototype/…`
- and is visible in the site navigation as **Material Prototype → Material Toggle / Material Checkbox / Material Input Field**.

---

## License & Legal Safety

Material&nbsp;3's implementation and documentation are available under the **MIT License**, which:

- permits reuse, modification, and redistribution,
- allows commercial use,
- does not enforce copyleft or require us to open-source TWE.

Because we are only re-using **design tokens** and not copying any implementation-specific source code verbatim, using M3 tokens as a baseline is **compatible with TWE’s goals** and does not preclude us from releasing TWE as our own design system.

---

**Legal Assurance** : Token Usage Falls Under MIT and Functional Design Rules

Material 3 is released under the MIT license, one of the most permissive open-source licenses available. MIT allows reuse, modification, and redistribution of code and design assets, including for commercial purposes.
Since this evaluation uses only M3 design tokens (color values, typography scales, shape radii, elevation metadata), and not Google’s source code or proprietary component implementations, it falls entirely within legally permitted use.

Design tokens represent functional design metadata, which is not copyrightable. Google explicitly intends for teams to adopt and adapt these tokens to build their own custom design systems, as stated in Material documentation.
As such, TWE’s usage of exported Material theme tokens is fully permitted, safe, and aligned with industry practice.
---

## Theme Builder Workflow (Figma → JSON → SCSS)

1. Use the **Material Theme Builder** Figma plugin to generate a theme.
2. Export the theme as JSON.
3. Save the export into the repo:  
   `docs/material-prototype/tokens/m3-export.json`
4. Select a small, meaningful subset of tokens (primary colors, surface, outline, shape radius, typography scale, elevation).
5. Map those values into SCSS variables:  
   `docs/material-prototype/tokens/_m3-tokens.scss`
6. Consume the tokens in prototype components:
   - `_toggle-m3.scss`
   - `_checkbox-m3.scss`
   - `_input-m3.scss`
7. For the MkDocs demo pages, compile the SCSS to CSS once and inline it inside:
   - `toggle.md`
   - `checkbox.md`
   - `input.md`

This establishes a clear pipeline:

**Figma → JSON → SCSS tokens → TWE components → MkDocs demo.**

---

## Prototype Findings

### 1. Toggle (Switch)

- Easily styled using:
  - `m3-color-primary` / `m3-color-on-primary`
  - `m3-color-outline`
  - `m3-radius-full`
  - `m3-elevation-1`
- States (checked, unchecked, focus) mapped cleanly to token roles.
- Implementation stayed in our HTML/SCSS; no Material code imported.

### 2. Checkbox

- Uses the same color + shape tokens as Toggle.
- Checkmark is built with pure CSS; background and border colors come from primary tokens.
- Demonstrates that **multiple components can share the same token set**, which is important for consistency.

### 3. Input Field

- Uses filled text-field pattern based on:
  - `m3-color-primary-container`
  - `m3-color-on-primary-container`
  - `m3-color-outline`
  - `m3-color-primary` for focus underline.
- Shows how typography and color tokens can align with our existing form-field patterns.

---

## Pros of Adopting M3 Tokens as a Baseline

- **Speed** – We can bootstrap new components quickly using a well-documented token set instead of inventing all roles from scratch.
- **Consistency** – Shared tokens across components naturally enforce consistent color/shape/typography usage.
- **Ecosystem Alignment** – M3 is widely used; having similar tokens makes it easier to integrate or reuse patterns from Material-based libraries when appropriate.
- **React Readiness** – If TWE eventually ships a React design-system package, M3-style tokens map cleanly to popular libraries (e.g., MUI) while still letting us own our HTML/SCSS.
- **Flexibility** – Tokens live in our SCSS layer; we can override or extend them without being locked into Google’s exact look.

---

## Risks / Considerations

- **Visual Identity** – If we adopt tokens 1:1 without adjustments, TWE may look too similar to “pure Google Material.” We should treat M3 as a baseline and then customize.
- **Migration Overhead** – Retrofitting existing components to use tokens requires some refactoring of our current SCSS (e.g., replacing hard-coded colors with token variables).
- **Partial Adoption** – We should be intentional about which token categories we adopt (colors, shape, elevation, etc.) to avoid an inconsistent half-Material / half-custom system.

---

## React Design System Implications

If we move toward a React design system:

- Having a structured token file (`_m3-tokens.scss` or a future JSON/TS token source) makes it straightforward to generate:
  - CSS variables,
  - JS/TS token objects,
  - and theming utilities.
- M3’s concepts (surface, primary container, etc.) align with theming APIs in libraries like MUI, but we still control the implementation.
- Starting with tokens **today** reduces future migration work for React.

---

## Recommendation: **Keep (Use as Token Baseline)**

Based on the prototype and research:

- ✅ **License** – MIT is safe and compatible with TWE’s goals.  
- ✅ **Implementation** – We successfully mapped tokens into SCSS and styled 3 components without importing Material’s source code.  
- ✅ **Scalability** – Tokens can be extended, themed, and later consumed by React or other front-ends.

**Recommendation:**  
Use Material&nbsp;3 as a **token baseline** (color, typography, shape, elevation) for TWE, while continuing to build **our own components and visual identity** on top of it.

Next steps if we continue:

1. Gradually refactor existing components (buttons, inputs, toggles, checkbox, etc.) to consume shared tokens instead of hard-coded values.
2. Align naming between TWE tokens and M3 roles to keep things understandable (e.g., `twe-color-primary` → `m3-color-primary`).
3. Consider a future token source of truth (JSON/TS) that can generate both SCSS variables and React theme objects.
