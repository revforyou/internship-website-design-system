# Material Prototype (M3 Tokens → TWE)

This folder contains a small prototype exploring how **Material&nbsp;3 tokens** can be used as a baseline for the TWE Design System.

## Goals

- Validate that tokens exported from the **Material Theme Builder** Figma plugin can be:
  - stored as JSON,
  - mapped into SCSS,
  - and consumed by our existing HTML/SCSS component architecture.
- Style 3 existing component types using those tokens:
  - Toggle (switch)
  - Checkbox
  - Input field
- Keep the prototype **isolated** from production CSS, but fully visible in the MkDocs site.

## Structure

- `tokens/`
  - `m3-export.json` – raw theme export from the Figma plugin.
  - `_m3-tokens.scss` – hand-picked subset of tokens mapped to SCSS variables.
- `components/`
  - `_toggle-m3.scss`
  - `_checkbox-m3.scss`
  - `_input-m3.scss`
- Root markdown demos:
  - `toggle.md`
  - `checkbox.md`
  - `input.md`

Each markdown page includes a small inline `<style>` block (compiled CSS) so the demos render even without wiring the SCSS into the main build. The SCSS files show how we would integrate these tokens more formally in the future.
