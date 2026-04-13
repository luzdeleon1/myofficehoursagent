
---

title: Date Picker – FAQ

---

# Date Picker

Frequently asked questions about the Date Picker component in the Design System.

---

## Date Picker not prompting date validation upon user interacting with input to type date.

**Answer**
This is a defect in Date Picker.

**Notes**
Date Picker by design is expected to prompt validation on Enter key press for Accessibility purposes, as it would be overwhelming non-sighted users that screen readers announce constantly error messages while user still types.

---

### Variants
## Range Picker

Range Picker is a variant of Date Picker to allow user to select from start date to end date.

---

## Give an example for Minimum Date and Maximum Date, in the Min date user can select today date and max date can be today +365?

**Answer**
If you need dynamically generated dates, you will have to calculate them, convert them to datetime strings and assign them as the relevant data attributes before initializing the date picker. 


**Example**
```javascript
let minDateString = new Date().toISOString(); // current date as string
let maxDateString = new Date(new Date().getTime() + 365 * 24 * 60 * 60 * 1000).toISOString(), // date 365 days from now as string
```

---

## Single Picker

Single Picker is a variant of Date Picker to allow user to select a single date in calendar

---
## Helper text in Date Picker is not showing up in Spanish when the user changes the language. It still shows MM/DD/YYYY instead of MM/DD/AAAA. Is this something that's missing from the pattern?

**Answer**
No.

**Notes**
Date picker has an attribute to sets the language for the build in strings: data-lang. Setting data-lang=”es” in your date picker element before initialization will initialize it using the default Spanish strings.

**References**
https://confluence-aes.kp.org/spaces/DSDOC/pages/535203191/Date+Picker#DatePicker-Javascript
