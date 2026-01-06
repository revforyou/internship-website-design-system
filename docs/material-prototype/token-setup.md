---
title: Material 3 Baseline Demo – Setup & Workflow
hide:
  - toc
---

# **Material 3 Baseline Demo – Setup & Workflow**

This page documents **how Material 3 was evaluated as a baseline** for the TWE Design System using a **non-invasive demo approach**.  
The goal was to validate Material tokens, states, and interaction patterns **without impacting production components**.

---

## 1. Using Material Theme Builder in Figma

We used the official **Material Theme Builder** Figma plugin to:

- Apply Material 3 color, shape, and typography systems in Figma
- Preview Material components (toggle, checkbox, inputs, etc.)
- Inspect interaction states (hover, focus, pressed, disabled)
- Export Material design tokens as JSON

This step was used **for reference and validation only**, not for direct production code.

---

## 2. Token Export & Mapping

The plugin exports a Material-compliant JSON structure similar to:

```json
{
  "schemes": {
    "light": {
      "primary": "#6750A4",
      "onPrimary": "#FFFFFF",
      "surface": "#FFFBFE",
      "outline": "#79747E"
    }
  }
}
```

Instead of importing this JSON directly into the build system, we **manually mapped relevant Material roles** into CSS variables for demo use:

```scss
[data-material] {
  --m3-primary: var(--color-primary);
  --m3-on-primary: var(--color-on-primary);
  --m3-surface: var(--color-surface);
  --m3-outline: var(--color-outline);
}
```

This ensured:
- No global CSS conflicts
- No changes to existing TWE tokens
- Full isolation of Material demo styles

---

## 3. Demo Component Implementation (SCSS)

To avoid overlap with existing components:

- New demo-only classes were created (e.g. `toggle-m3`, `checkbox-m3`)
- Existing TWE components were not modified
- All Material demos are wrapped in a scoped container:

```html
<div data-material>
  <!-- Material demo component -->
</div>
```

Each demo component:
- Follows Material proportions, motion, and state behavior
- Reads values from `m3-tokens.scss`
- Is fully isolated from production styles

---

## 4. Markdown Demos (.md)

Each Material demo includes:

- Base class usage
- Full state coverage:
  - Default
  - Hover
  - Focus
  - Pressed
  - Disabled
- Variants with and without icons
- Variants with and without labels (where applicable)

This mirrors existing TWE documentation patterns for easy comparison.

---

## 5. Why This Approach

This workflow allowed us to:

- Evaluate Material 3 without refactoring the design system
- Identify CSS collision risks early
- Validate token and state compatibility
- Establish a repeatable pattern for future demos

---

## 6. Final Outcome

- Material 3 can be used as a **baseline reference**
- Tokens, motion, and interaction states map cleanly to TWE concepts
- Full adoption would require deeper token integration
- Demo-based evaluation is the safest and clearest path forward

This concludes the Material 3 baseline evaluation.
