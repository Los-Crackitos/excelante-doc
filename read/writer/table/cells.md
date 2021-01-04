### Write cells

Cells represent an array of cells values.

```json
"cells": [{
  "value":"",
  "style": {},
  "is_formula": true
}]

```

Cell object contains these fields :

- `value ` that represent cell data
- `style `that represent cell style (e.g border, fill, ...)
- `is_formula`determine if cell value is a formula. This field is optionnal, set to `false` by default.
