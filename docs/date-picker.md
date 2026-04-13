# Date Picker

## Pattern Properties
- Package Name: datepicker-pattern
- DS1: Yes
- Vessel: Yes
- Foundation: Yes

## Installation

### Prerequisite
```bash
npm install styleguide
```

### Install
```bash
npm install datepicker-pattern
```

## Usage

### Styling (DS1)
```scss
@import 'styleguide/modern';
@import 'datepicker-pattern/datepicker-ds1';
```

### Styling (Vessel)
```scss
@import 'styleguide/styleguide-ds2';
@import 'datepicker-pattern/datepicker';
```

### Styling (Foundation)
```scss
@use 'datepicker-pattern/datepicker-foundation';
```

## HTML Examples

### Single Date Picker
```html
<div class="date-range-single"></div>
```

### With Options
```html
<div
  class="date-range-single"
  data-default-date="February 15 2024"
  data-min-date="January 1 2024"
  data-max-date="December 31 2024"
></div>
```

### Vessel Version
```html
<div
  class="ds-datepicker"
  data-date-selector="single"
  data-ds-theme="Vessel"
></div>
```

## JavaScript

```js
import { datePickerSingleInit } from 'datepicker-pattern/src/date-picker';

datePickerSingleInit('.date-range-single');
```

## Events
- `changeDate` → returns selected date

## Options
- `lang`
- `minDate`
- `maxDate`
- `defaultDate`

## Notes
- Defaults to English
- Supports Spanish (`lang: "ES"`)
- Inline errors handled automatically
