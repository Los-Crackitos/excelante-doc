# Write items

Items represent an array of all data that can be writed on Excel sheet.

```javascript
"items": [{
  "starting_cell_coordinates": "B3",
  "table": [{}],
  "chart": {}
}]
```

Items contains the following fields :

* `starting_cell_coordinates` represent the position of the first element that will be written on the Excel sheet
* `table` contains an array of all the table data.
* `chart` represent a chart object

