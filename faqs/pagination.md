
---
title: Pagination – FAQ
---

# Pagination

Frequently asked questions about the Pagination component in the Design System.

---
## Pagination pattern wasn't displaying correctly

**Description**
The Pagination pattern wasn't displaying correctly in the DOM

**Symptoms**
The user may experience one or more of the following symptoms:
- Misaligned or overlapping elements
- Broken styles (CSS errors)
- “Invisible” content
- Erratic pattern behavior
- Accessibility issues: Confusing screen readers, Keyboard navigation blocked

**Possible Causes**
This problem may occur because:
- invalid markup
- Unclosed Tags
- Class Name Mismatches

**Answer**
Implement correct HTML

**Example**
```html
<div class="pagination-pattern" data-ds-version="1"></div> <!---Stands for Vessel with old pagination classes-->

<!--Pagination with JS Rendered Dropdown for Mobile view navigation-->
<div class="ds-pagination" data-ds-version="2" data-ds-variant="basic"></div> <!---data-ds-version="2" stands for for Vessel with new pagination classes-->
<div class="ds-pagination" data-ds-version="2" data-ds-variant="static-dropdown"></div> <!---data-ds-version="2" stands for for Vessel with new pagination classes-->

<!--Pagination with JS Rendered Dropdown for Mobile view navigation-->
<div class="ds-pagination" data-ds-version="3" data-ds-variant="basic"></div> <!---data-ds-version="3" stands for for Vessel Foundation with new pagination classes-->
<div class="ds-pagination" data-ds-version="3" data-ds-variant="static-dropdown"></div> <!---Stands for Vessel Foundation-->

```


**Note**
Pagination uses Dropdown to render user navigation in Mobile view
It is important to describe the variant to use as it determines how Dropdown will be rendered for mobile view functionality

**References**
https://confluence-aes.kp.org/spaces/DSDOC/pages/485800361/Pagination
https://fed.kp.org/storybook/?path=/story/patterns-pagination-vessel--pagination
ttps://fed.kp.org/storybook/?path=/story/patterns-pagination-vessel--pagination-static-dropdown
https://fed.kp.org/storybook/?path=/story/patterns-pagination-vessel--pagination-navigation&globals=viewer:On

---

## How to handle pagination buttons functionality?

**Description**
After integrating the markup, I don't know how to make the buttons on the pages work

**Symptoms**
The user may experience one or more of the following symptoms:
- Buttons do not work
- You cannot navigate to the next or previous page

**Possible causes**
This problem may occur because:
- invalid markup
- Class Name Mismatches

**Answer**
Correct markup

**Notes**
Pagination current version  includes a version with button handling functionality which is called "Navigation".
data-total-items= is required attribute.
data-items-per-page is required attribute
data-asset-src is required attribute
data-assets-src-dropdown is optional attribute

**Example**
```html
<!---  Here is the markup for Navigation pagination with **JS rendered Dropdown**: -->

<pre><code>
<div class="ds-pagination" data-ds-theme="vessel" data-ds-variant="navigation" data-ds-version="2"
      data-total-items="100" data-items-per-page="10" data-asset-src="assets/images/">
        <div class="ds-pagination__count">
          <p role="status" aria-atomic="true">
            <span class="ds-pagination__fromToIndexTxt"></span>
          </p>
        </div>
        <nav class="ds-pagination__nav" role="navigation">
          <ul class="ds-pagination__list ds-pagination__desktop-list">
          </ul>
          <span>
            <p class="back-label --desktop-label" aria-hidden="true">Previous results</p>
          </span>
          <span>
            <p class="forward-label --desktop-label" aria-hidden="true">Next results</p>
          </span>
          <div class="ds-pagination__list ds-pagination__mobile-list">
            <div class="ds-pagination__item -prev -disabled">
              <a class="ds-pagination__link" href="#" tabindex="-1" aria-disabled="true">
                <span class="screenreader-only">Pagination reached first page</span>
                &lt;svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true" class="icon-chevron-back"&gt;
                  &lt;use href="assets/images/arrowbackios.svg#arrowbackios"&gt;&lt;/use&gt;
                &lt;/svg&gt;
              </a>
              <span>
                <p class="back-label" aria-hidden="true">Previous results</p>
              </span>
            </div>
            <div
              class="ds-dropdown"
              data-ds-theme="vessel"
              data-ds-variant="basic"
              data-ds-version="2"
              data-list-type="option"
              data-menu-type="standard"
              data-select-label="selected"
            >
              <div class="ds-dropdown__drop-menu">
                <label class="ds-dropdown__label"></label>
                <button class="ds-dropdown__trigger-button ds-paginationTrigger">
                  <span class="ds-dropdown__trigger-text">Selected Element</span>
                  <img class="ds-dropdown__chevron" src="assets/images/chevrondown.svg" alt="" width="24" height="24" />
                </button>
                <ul class="ds-dropdown__menu-list paginationList"></ul>
              </div>
            </div>
            <div class="ds-pagination__item -page">
              <a class="ds-pagination__link" href="#">
                <span class="screenreader-only">page</span>
                <span class="ds-pagination__pageIndex">20</span>
              </a>
            </div>
            <div class="ds-pagination__item -next">
              <a class="ds-pagination__link" href="#" title="Go to Page 2">
                <span class="screenreader-only">Next result</span>
                &lt;svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true" class="icon-chevron-forward"&gt;
                  &lt;use href="assets/images/arrowbackios.svg#arrowbackios"&gt;&lt;/use&gt;
                &lt;/svg&gt;
              </a>
              <span>
                <p class="forward-label" aria-hidden="true">Next results</p>
              </span>
            </div>
          </div>
        </nav>
      </div>
</pre>

<!---  Here is the markup for Navigation pagination with **Static HTML Dropdown**: -->

<pre><code>
    <div class="ds-pagination ds-pagination__static-dropdown" data-ds-theme="vessel" data-ds-variant="navigation" data-ds-version="2"
      data-total-items="100" data-items-per-page="10" data-asset-src="assets/images/">
        <div class="ds-pagination__count">
          <p role="status" aria-atomic="true">
            <span class="ds-pagination__fromToIndexTxt"></span>
          </p>
        </div>
        <nav class="ds-pagination__nav" role="navigation">
          <ul class="ds-pagination__list ds-pagination__desktop-list">
          </ul>
          <span>
            <p class="back-label --desktop-label" aria-hidden="true">Previous results</p>
          </span>
          <span>
            <p class="forward-label --desktop-label" aria-hidden="true">Next results</p>
          </span>
          <!-- Mobile -->
          <div class="ds-pagination__list ds-pagination__mobile-list">
            <div class="ds-dropdown" data-init-type="static"
              data-ds-theme="vessel"
              data-ds-variant="basic"
              data-ds-version="2"
              data-list-type="option"
              data-select-label="selected"
              data-context-type="select">
              <div class="ds-dropdown__drop-menu">
                <label class="ds-dropdown__label screenreader-only">
                  <!-- image used in area data-menu-type only -->
                  <span class="ds-dropdown__label-text">pagination</span>
                </label>
                <button class="ds-dropdown__trigger-button ds-paginationTrigger">
                  <span class="ds-dropdown__trigger-text"></span>
                  <img class="ds-dropdown__chevron" src="assets/images/chevrondown.svg" alt="" width="24" height="24">
                </button>
                <ul class="ds-dropdown__menu-list paginationList">
                  <li class="drop-menu-list-op active" tabindex="-1" data-selected="true" data-name="Page 1">
                    <span class="drop-menu-list-text">Page 1</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 2">
                    <span class="drop-menu-list-text">Page 2</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 3">
                    <span class="drop-menu-list-text">Page 3</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                   
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 4">
                    <span class="drop-menu-list-text">Page 4</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 5">
                    <span class="drop-menu-list-text">Page 5</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 6">
                    <span class="drop-menu-list-text">Page 6</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 7">
                    <span class="drop-menu-list-text">Page 7</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 8">
                    <span class="drop-menu-list-text">Page 8</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 9">
                    <span class="drop-menu-list-text">Page 9</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                  <li class="drop-menu-list-op" tabindex="-1" data-selected="false" data-name="Page 10">
                    <span class="drop-menu-list-text">Page 10</span>
                    <img class="checkmark-img" alt="" src="assets/images/checkmark-black.svg" width="24" height="24" />
                  </li>
                </ul>
              </div>
            </div>
            <div class="ds-pagination__item -page">
              <a class="ds-pagination__link" href="#">
                <span class="screenreader-only">page</span>
                <span class="ds-pagination__pageIndex">20</span>
              </a>
            </div>
          </div>
          <!-- Mobile ends -->
        </nav>
      </div>
<pre><code>
```