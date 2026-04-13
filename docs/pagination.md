# Pagination

## Pattern Properties
- Pattern Name: Pagination-pattern
- Version: 7.1.0
- DS1: Yes
- Vessel: Yes
- JS Pattern: Yes
- Dependencies: dropdown-menu-pattern

## Installation

### Prerequisites
```bash
npm install styleguide
```

### Install
```bash
npm install pagination-pattern
```

### package.json
```json
"pagination-pattern": "7.1.0"
```

## Usage

### Styling

#### DS1
```scss
@import 'styleguide/global-main';
@import 'styleguide/lib/modern/stylesheets/kp-icons';
@import 'pagination-pattern/pagination-ds1';
```

#### Vessel
```scss
@import 'styleguide/styleguide-ds2';
@import 'dropdown-menu-pattern/dropdown-menu';
@import 'pagination-pattern/pagination';
```

#### Foundation
```scss
@use 'pagination-pattern/pagination-foundation';
```

### JavaScript

```js
import { paginationInitAll } from './pagination';
import { dropMenuInit } from './dropdown-menu-pattern';

document.onreadystatechange = function () {
  if (document.readyState === 'complete') {
    dropMenuInit();
    paginationInitAll();
  }
};
```

## HTML Example

```html
<div class="kpPagination">
  <div class="kpPagination__count">
    <p>1 - 10 of 50 items</p>
  </div>
</div>
```

## Scenarios
- Static count
- Navigation with pages
- Disabled states
- Active page highlighting
