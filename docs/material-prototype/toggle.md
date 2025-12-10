---
hide:
  - toc
---

<style>
/* ================================
   MATERIAL 3-STYLE TOGGLE DEMO
   Scoped to [data-material] area
   ================================ */

[data-material] {
  --m3-primary: #6750A4;
  --m3-on-primary: #FFFFFF;
  --m3-surface: #FFFBFE;
  --m3-on-surface: #1C1B1F;
  --m3-outline: #79747E;
  --m3-surface-variant: #E7E0EC;

  --m3-focus-ring: rgba(103, 80, 164, 0.35);
  --m3-hover-ring: rgba(103, 80, 164, 0.16);
  --m3-pressed-ring: rgba(103, 80, 164, 0.22);

  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

/* Center single demo components horizontally */
[data-material] .btn-grid-1 {
  display: flex;       /* instead of inline-flex */
  justify-content: center;
  align-items: center;
}


[data-material] .grid-items {
  border: 1px solid #e0e0e0;
  padding: 1.5rem;
  border-radius: 0.75rem;
  background: #fafafa;
}

/* Base toggle track */
[data-material] .toggle {
  position: relative;
  display: inline-block;
  width: 52px;
  height: 32px;
  padding: 2px 4px;
  border-radius: 100px;

  background-color: var(--m3-surface);
  box-shadow: inset 0 0 0 1px var(--m3-outline);
  transition: background-color 0.25s ease, box-shadow 0.25s ease, transform 0.2s ease;
}

/* Hide native checkbox */
[data-material] .toggle input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* Thumb */
[data-material] .toggle .slider {
  position: absolute;
  cursor: pointer;
  left: 4px;
  bottom: 4px;
  width: 24px;
  height: 24px;

  background-color: var(--m3-outline);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;

  color: var(--m3-surface);
  transition: background-color 0.25s ease, transform 0.25s ease, box-shadow 0.25s ease;
}

/* Checked state (track + thumb) */
[data-material] .toggle input:checked + .slider {
  background-color: var(--m3-on-primary);
  color: var(--m3-primary);
  transform: translateX(20px);
}

[data-material] .toggle:has(input:checked) {
  background-color: var(--m3-primary);
  box-shadow: none;
}

/* Icons logic (checked/unchecked spans) */
[data-material] .toggle .slider .checked {
  display: none;
}

[data-material] .toggle .slider .unchecked {
  display: block;
}

[data-material] .toggle input:checked + .slider .checked {
  display: block;
}

[data-material] .toggle input:checked + .slider .unchecked {
  display: none;
}

/* Hover state (matches your .hover class) */
[data-material] .toggle.hover input:not(:disabled) + .slider {
  box-shadow: 0 0 0 6px var(--m3-hover-ring);
}

/* Focus state (matches your .focus class) */
[data-material] .toggle.focus input:not(:disabled) + .slider {
  box-shadow: 0 0 0 6px var(--m3-focus-ring);
}

/* Pressed state (matches your .active class) */
[data-material] .toggle.active input:not(:disabled) + .slider {
  transform: translateX(20px) scale(0.9);
  box-shadow: 0 0 0 6px var(--m3-pressed-ring);
}

/* Disabled states */
[data-material] .toggle input:disabled + .slider {
  background-color: var(--m3-surface-variant);
  color: #b0a7c0;
  cursor: not-allowed;
}

[data-material] .toggle:has(input:disabled) {
  background-color: #f4f0f8;
  box-shadow: inset 0 0 0 1px #d0c7dd;
  cursor: not-allowed;
}
</style>

# **Material Baseline: Toggle (Scoped)**

This page shows how our existing **Toggle component** behaves when placed inside a **Material&nbsp;3 baseline**, reusing the same HTML structure, classes, and state variations as the TWE documentation — but restyled with M3 colors, radii, and state treatments.

Everything below is wrapped in a `data-material` container so it does **not** affect the rest of the design system.

---

## Class

=== "Selected No Icon"
    <div data-material>
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox" checked>
                    <span class="slider">
                    </span>
                </label>
            </div>
        </div>
    </div>
    <br>
    ## **States**
    === "Default"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items"> 
                    <label class="toggle hover">
                        <input type="checkbox" checked>
                        <span class="slider"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Hover"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items"> 
                    <label class="toggle">
                        <input type="checkbox" checked>
                        <span class="slider"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Focused"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items"> 
                    <label class="toggle focus">
                        <input type="checkbox" checked>
                        <span class="slider"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Pressed"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items"> 
                    <label class="toggle active">
                        <input type="checkbox" checked>
                        <span class="slider"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Disabled"
        <div data-material>       
            <div class="btn-grid-1">
                <div class="grid-items"> 
                    <label class="toggle">
                        <input type="checkbox" checked disabled>
                        <span class="slider"></span>
                    </label>
                </div>
            </div>
        </div>

    <br>

    ## Code
    === "CSS (Material Baseline Prototype)"
        ```css
        .toggle {
          /* Material-like baseline styles applied in the prototype */
          /* See material-prototype/components/_toggle-m3.scss for full mapping */
        }
        ```

    === "HTML"
        ```html
        <label class="toggle">
          <input type="checkbox" checked>
          <span class="slider"></span>
        </label>
        ```

=== "Selected w/ Icon"
    <div class="btn-grid-1">
        <div class="grid-items"> 
            <label class="toggle">
                <input type="checkbox" checked>
                <span class="slider">
                    <span class="checked">✔</span>
                    <span class="unchecked">✕</span>
                </span>
            </label>
        </div>
    </div>
    <br>
    ## **States**
    === "Default"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox" checked>
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    === "Hover"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle hover">
                    <input type="checkbox" checked>
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    === "Focused"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle focus">
                    <input type="checkbox" checked>
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    === "Pressed"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle active">
                    <input type="checkbox" checked>
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    === "Disabled"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox" checked disabled>
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    <br>

    
    === "CSS (Material Baseline Prototype)"
        ```css
        .toggle .slider .checked { /* visible when checked */ }
        .toggle .slider .unchecked { /* visible when not checked */ }
        ```

    === "HTML"
        ```html
        <label class="toggle">
          <input type="checkbox" checked>
          <span class="slider">
            <span class="checked">✔</span>
            <span class="unchecked">✕</span>
          </span>
        </label>
        ```

=== "De-Selected No Icon"
    <div class="btn-grid-1">
        <div class="grid-items"> 
            <label class="toggle">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
    </div>
    <br>
    ## **States**
    === "Default"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox">
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    === "Hover"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle hover">
                    <input type="checkbox">
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    === "Focused"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle focus">
                    <input type="checkbox">
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    === "Pressed"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle active">
                    <input type="checkbox">
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    === "Disabled"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox" disabled>
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    <br>

    ## Code

    === "HTML"
        ```html
        <label class="toggle">
          <input type="checkbox">
          <span class="slider"></span>
        </label>
        ```

=== "De-Selected w/ Icon"
    <div class="btn-grid-1">
        <div class="grid-items"> 
            <label class="toggle">
                <input type="checkbox">
                <span class="slider">
                    <span class="checked">✔</span>
                    <span class="unchecked">✕</span>
                </span>
            </label>
        </div>
    </div>
    <br>
    ## **States**
    === "Default"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox">
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    === "Hover"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle hover">
                    <input type="checkbox">
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>
                </label>
            </div>
        </div>
    === "Focused"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle focus">
                    <input type="checkbox">
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>                
                </label>
            </div>
        </div>
    === "Pressed"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle active">
                    <input type="checkbox">
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>   
                </label>
            </div>
        </div>
    === "Disabled"
        <div class="btn-grid-1">
            <div class="grid-items"> 
                <label class="toggle">
                    <input type="checkbox" disabled>
                    <span class="slider">
                        <span class="checked">✔</span>
                        <span class="unchecked">✕</span>
                    </span>   
                </label>
            </div>
        </div>

    <br>

    ## Code
    === "HTML"
        ```html
        <label class="toggle">
          <input type="checkbox">
          <span class="slider">
            <span class="checked">✔</span>
            <span class="unchecked">✕</span>
          </span>
        </label>
        ```

