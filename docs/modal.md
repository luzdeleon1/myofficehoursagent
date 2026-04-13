
---
title: Modal – FAQ
---

# Modal

Frequently asked questions about the Modal component in the Design System.

---

## Spacing issues after updating Modal from 5.7.0 version to 6.1.1

**Answer**
It is necessary to make updates to markup according to 6.1.1 version


**Notes**
Updating package is one step but given the major package update

---

## Layout issues in Modal

**Answer**
Do not implement Legacy Modal.


**References**
https://jira-aes.kp.org/browse/IAM1-26391

---

## Two Modal instances used but trigger buttons only open the same Modal Instance.

**Answer**
Double check that each trigger element's data-modal-trigger attribute points to a unique ID of each Modal

**Example**
```html
<!--Buttons-->
<button class="button" data-modal-trigger="modal-1">Open Modal 1</button>
<button class="button" data-modal-trigger="modal-2">Open Modal 2</button>

<!--Modals-->
<div class="ds-modal" id="modal-1"></div>
<div class="ds-modal" id="modal-2"></div>
```

---

### Variants
## Full Screen

Fulll screen is a variant of Modal to display content in a content window that uses full screen width
---

## Window Screen

Window screen is the basic variant of Modal to display content in a content window

---