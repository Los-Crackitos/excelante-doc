# Write a sheet

Excelante writer take a JSON input that contain an array of sheets.

```javascript
{
  "sheets": [{
    "name": "Sheet1",
    "orientation": "OrientationLandscape",
    ...
  }, {
    "name": "Sheet2",
    "orientation": "OrientationPortrait",
    ...
  }, {
    ...
  }]
}
```

Sheets have some values to define their characteristics :

* An orientation, that can be `OrientationLandscape` or `OrientationPortrait`
* An array of `Items`

