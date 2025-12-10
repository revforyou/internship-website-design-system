---
hide:
  - toc
---

# Material Input Field (Prototype)

> Filled text field based on Material&nbsp;3 tokens, wired into TWE via our own HTML and SCSS.

<style>
.m3-text-field {
  display: inline-flex;
  flex-direction: column;
  gap: 4px;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  font-size: 16px;
  line-height: 24px;
  color: #1C1B1F;
  padding: 1.5rem 0;
}
.m3-text-field__label {
  font-size: 14px;
  line-height: 20px;
  color: #1C1B1F;
}
.m3-text-field__input {
  min-width: 280px;
  padding: 12px 16px;
  border-radius: 8px 8px 0 0;
  border: none;
  border-bottom: 1px solid #79747E;
  background-color: #EADDFF;
  color: #21005D;
  font: inherit;
  outline: none;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
.m3-text-field__input::placeholder {
  color: rgba(33, 0, 93, 0.6);
}
.m3-text-field__input:focus {
  border-bottom-color: #6750A4;
  box-shadow: 0 1px 0 0 #6750A4;
}
</style>

<div class="m3-text-field">
  <span class="m3-text-field__label">Email</span>
  <input
    type="email"
    class="m3-text-field__input"
    placeholder="name@example.com"
  />
</div>

## Token Mapping

- **Primary container (`#EADDFF`)** – field background.
- **On primary container (`#21005D`)** – input text color.
- **Outline (`#79747E`)** – resting underline.
- **Primary (`#6750A4`)** – focused underline + focus shadow.

Source SCSS:  
`docs/material-prototype/components/_input-m3.scss`
