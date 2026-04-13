# Modal

## Pattern Properties
- Pattern Name: modal-pattern
- Version: 7.2.4
- DS1: Yes
- Vessel: Yes
- JS Pattern: Yes
- Dependencies: Dropdown menu, Print Utility, Slider

## Installation

### Prerequisites
```bash
npm install styleguide
```

### Install
```bash
npm install modal-pattern
```

### package.json
```json
"modal-pattern": "~7.2.1"
```

## Variants
- Windowed
- Fullscreen

### Column Options
- columns-4
- columns-6
- columns-8
- columns-10

## Usage

### Styling (DS1)
```scss
@import 'styleguide/global-main';
@import 'modal-pattern/modal-ds1';
```

### Styling (Vessel)
```scss
@import 'styleguide/styleguide-ds2';
@import 'modal-pattern/modal';
```

### Styling (Foundation)
```scss
@use 'modal-pattern/modal-foundation';
```

## HTML Example

```html
<div class="modal-pattern">
  <div class="modal-container">
    <div class="modal-inner" role="dialog">
      <button class="-close--small"></button>
    </div>
  </div>
</div>
```

## Accessibility Notes
- Use `aria-label` or `aria-labelledby`
- Manage `aria-hidden` state
- Ensure focus trapping
