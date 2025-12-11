---
title: Material Token Setup Guide
hide:
  - toc
---

# **Material Theme Tokens (Figma → JSON → TWE Prototype)**

This page documents how Material 3 tokens are generated using the **Material Theme Builder** Figma plugin, how the exported JSON is structured, and how these tokens are mapped into the **TWE Design System prototype**.

This satisfies the action item:

> **“Set up theme using Material UI Theme Figma Plugin, export JSON, and document basic steps.”**

---

## 1. What the Material Theme Builder Plugin Does

The **Material Theme Builder** plugin (official Google plugin) allows us to:

1. Apply Material 3 color, type, and shape systems inside Figma  
2. Generate tokens for:
   - Color roles  
   - Elevation  
   - Shape radii  
   - Typography  
3. Export these tokens as a **Material-compliant JSON file**  
4. Re-import or synchronize design + code tokens later

When exporting a theme, the plugin gives a JSON structure similar to:

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

## 2. How the JSON Would Be Integrated Into TWE (Future Step)

We are not fully converting TWE to Material 3, but if we did, the flow would be:

1. Export JSON →

2. Convert JSON tokens into SCSS variables →

3. Map SCSS variables into component styles →

4. The design system builds components from these tokens.

For example:

:root {
  --m3-primary: #6750A4;
  --m3-on-primary: #FFFFFF;
  --m3-surface: #FFFBFE;
  --m3-outline: #79747E;
}

## 3. How We Used Tokens Inside the Prototype

Because the full token system is not integrated into the build yet, we:

1. Scoped Material 3 tokens inside <div data-material>

2. Avoided interfering with the existing TWE styles

3. Mapped Material tokens only to the prototype toggle, checkbox, and input

Example from the toggle demo:

[data-material] {
  --m3-primary: #6750A4;
  --m3-on-primary: #FFFFFF;
  --m3-surface: #FFFBFE;
  --m3-outline: #79747E;
}

## 4. Why This Approach Is Useful

1. It allows us to evaluate Material 3 compatibility without changing our DS.

2. It shows how tokens influence color, focus rings, radii, and motion.

3. It provides a foundation for future automated token integration.