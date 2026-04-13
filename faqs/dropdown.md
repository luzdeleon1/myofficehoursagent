
---
title: Dropdown Menu – FAQ

---

# Dropdown Menu

Frequently asked questions about the Dropdown Menu component in the Design System.

---

## How to add 2 dropdown-menus on our page where dropdown should show 'Select an option' text on initial load.

**Answer**
Try adding your default text inside the "drop-down-button-text"
**Example**
```html
<div class="drop-menu-pattern --default" data-menu-type="standard">
              <div class="drop-menu">
                <label class="drop-menu-label"></label>
                <button class="drop-menu-dropdown --no-icon kpPaginationTrigger">
                  <span class="drop-menu-button-text">Select an option</span>
                  <img class="drop-down-menu-chevron" src="../_images/chevrondown.svg" alt="">
                </button>
                <ul class="drop-menu-list paginationList"></ul>
              </div>
            </div>
 ```
---

## Do you have a multi-select dropdown component?

**Answer**
No. There isn't a multi select dropdown within the library.

---
### Variants
## Region Picker

Region picker is a variant of Dropdown menu

---

## Is region picker component built w/ icon? There was no icon in Fedstory book.

**Answer**
Yes. The Region Picker variant includes an icon that matches the design specifications.
Although the Fed Storybook demo currently does not display it, the correct icon is `Pincross.svg`.


**References**
https://fed.kp.org/storybook/?path=/story/patterns-dropdown-menu-vessel--dropdown-region&globals=viewer:On
https://fed.kp.org/storybook/?path=/story/elements-system-icons-ds2--default-system-icons 

---
