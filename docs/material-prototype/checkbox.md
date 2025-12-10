---
hide:
  - toc
---

# Material Checkbox (Prototype)

> Material&nbsp;3–inspired checkbox built on top of shared design tokens. This prototype shows how M3 color, shape, and typography tokens can be mapped into a TWE component.

<style>
.m3-checkbox {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  font-size: 16px;
  line-height: 24px;
  color: #1C1B1F;
  margin-right: 2rem;
}
.m3-checkbox__native-control {
  position: absolute;
  opacity: 0;
  pointer-events: none;
}
.m3-checkbox__box {
  width: 18px;
  height: 18px;
  border-radius: 4px;
  border: 2px solid #79747E;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background-color: #FFFBFE;
  transition: background-color 0.15s ease, border-color 0.15s ease;
}
.m3-checkbox__checkmark {
  width: 10px;
  height: 10px;
  border-right: 2px solid #FFFFFF;
  border-bottom: 2px solid #FFFFFF;
  transform: rotate(45deg) scale(0);
  transform-origin: center;
  transition: transform 0.15s ease;
}
.m3-checkbox__native-control:checked + .m3-checkbox__box {
  background-color: #6750A4;
  border-color: #6750A4;
}
.m3-checkbox__native-control:checked + .m3-checkbox__box .m3-checkbox__checkmark {
  transform: rotate(45deg) scale(1);
}
</style>

<div style="padding: 1.5rem 0; display:flex; align-items:center;">
  <label class="m3-checkbox">
    <input type="checkbox" class="m3-checkbox__native-control" checked />
    <span class="m3-checkbox__box">
      <span class="m3-checkbox__checkmark"></span>
    </span>
    <span>Remember me</span>
  </label>

  <label class="m3-checkbox">
    <input type="checkbox" class="m3-checkbox__native-control" />
    <span class="m3-checkbox__box">
      <span class="m3-checkbox__checkmark"></span>
    </span>
    <span>Receive updates</span>
  </label>
</div>

## Token Mapping

- **Primary (`#6750A4`)** – background + border when checked.
- **On primary (`#FFFFFF`)** – checkmark color.
- **Surface (`#FFFBFE`)** – idle background.
- **Outline (`#79747E`)** – idle border.

Source SCSS:  
`docs/material-prototype/components/_checkbox-m3.scss`
