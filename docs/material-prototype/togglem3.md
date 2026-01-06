---
hide:
  - toc
---

# **Toggle (Material 3 Demo)**

This page demonstrates how our Toggle component behaves when placed inside a **Material 3 baseline**.

Everything is wrapped in a `data-material` container so it does **not affect production components**.

---

## Class

=== "Selected No Icon"
    <div data-material>
        <div class="btn-grid-1">
            <div class="grid-items">
                <label class="toggle-m3">
                    <input type="checkbox" checked>
                    <span class="toggle-m3__thumb"></span>
                </label>
            </div>
        </div>
    </div>
    ## States
    === "Default"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Hover"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Focused"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 focus">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Pressed"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 active">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Disabled"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" checked disabled>
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>

=== "Selected w/ Icon"
    <div data-material>
        <div class="btn-grid-1">
            <div class="grid-items">
                <label class="toggle-m3">
                    <input type="checkbox" checked>
                    <span class="toggle-m3__thumb">
                        <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                        <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                    </span>
                </label>
            </div>
        </div>
    </div>
    ## States
    === "Default"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Hover"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Focused"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 focus">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Pressed"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 active">
                        <input type="checkbox" checked>
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Disabled"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" checked disabled>
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>

=== "De-Selected No Icon"
    <div data-material>
        <div class="btn-grid-1">
            <div class="grid-items">
                <label class="toggle-m3">
                    <input type="checkbox">
                    <span class="toggle-m3__thumb"></span>
                </label>
            </div>
        </div>
    </div>
    ## States
    === "Default"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Hover"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Focused"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 focus">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Pressed"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 active">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>
    === "Disabled"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" disabled>
                        <span class="toggle-m3__thumb"></span>
                    </label>
                </div>
            </div>
        </div>

=== "De-Selected w/ Icon"
    <div data-material>
        <div class="btn-grid-1">
            <div class="grid-items">
                <label class="toggle-m3">
                    <input type="checkbox">
                    <span class="toggle-m3__thumb">
                        <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                        <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                    </span>
                </label>
            </div>
        </div>
    </div>
    ## States
    === "Default"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Hover"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Focused"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 focus">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Pressed"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3 active">
                        <input type="checkbox">
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
    === "Disabled"
        <div data-material>
            <div class="btn-grid-1">
                <div class="grid-items">
                    <label class="toggle-m3">
                        <input type="checkbox" disabled>
                        <span class="toggle-m3__thumb">
                            <span class="toggle-m3__icon toggle-m3__icon--checked">check</span>
                            <span class="toggle-m3__icon toggle-m3__icon--unchecked">close</span>
                        </span>
                    </label>
                </div>
            </div>
        </div>
