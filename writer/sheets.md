### Write a sheet

Excelante writer take a json input that contain an array of sheets.

```json
{
  "sheets": [{
    "name": "Sheet1",
    ...
  }, {
    "name": "Sheet2",
    ...
  }, {
    ...
  }]
}

```

Sheets have some values to define their characteristics :

- An orientation, that can be ``` OrientationLandscape ``` or ``` OrientationPortrait ```
- An array of ```Items ```
