# Write table

A table take an array of `ColOrRowValues` objects. All object contains a column or a row dataset.

```javascript
"table": [{
  "orientation": "column",
  "cells": [{}]
}]
```

Table contains the following fields :

* `orientation` define writer comportment. Value can be `column` or `row`. By default, value is set to `column`.
* An array of `cells` that contain all `column` or `row`values

