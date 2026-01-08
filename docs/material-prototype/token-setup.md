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

- Use the **Material 3 Design Kit + Theme Builder** in Figma.
- Place the relevant Material components (toggle, checkbox, inputs, etc.) in the workspace.
- Use these components to identify:
  - Required states (default, hover, focus, pressed, disabled)
  - Icon usage
  - Sizing, spacing, and motion expectations

Material is used here as the **design reference**, not as a UI library.


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

- Export tokens from Material Theme Builder (JSON).
- Do **not** replace existing TWE tokens.
- Map Material roles into a shared SCSS token file (`m3-tokens.scss`).

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

- This token file is **extended over time** as new components are added.
- Tokens are defined once and reused across components.


---

## 3. Demo Component Implementation (SCSS)

- New components follow Material-defined structure and states.
- Implement components using mapped Material tokens.
- Use **new, isolated classes** (e.g. `toggle-m3`, `checkbox-m3`) to avoid collisions.
- Existing TWE components are not modified.

All Material-based components are scoped using:
```html
<div data-material>
  <!-- component -->
</div>
```
---

## 4. Markdown Demos (.md)

Each Material component includes:

- Document components using existing TWE markdown patterns.
- Include: Base class, All required states,Variants (icons, labels if applicable)
- Layout tweaks are allowed, but core behavior follows Material definitions.
---

## 5. Why This Approach

This workflow allowed us to:

- Evaluate Material 3 as baseline for new components without refactoring the design system
- Validate token and state compatibility
- Establish a repeatable pattern for future components

---

## 6. Final Outcome

- Material 3 provides the **baseline definitions** for component structure, states, and interaction.  
- TWE implements these definitions using its own tokens, SCSS, and documentation patterns, enabling faster and more consistent development of new components.

This concludes the Material 3 baseline evaluation.
