# Readers

## Read Excel file by lines

Make a call to `/api/v1/read/lines` route to read a file lines by lines.

An input file need to be sent during the POST method. Only multipart file data are acceptable as input.

For example:

```bash
curl -F file=@testFiles/input.xlsx http://localhost:8000/api/v1/read/lines --output myFile.json
```

This API route read line by line an given spreadsheet file and return a JSON with all values inside the file.

Example return value:

```javascript
{
  "Suivi charge": {
    "1": ["févr. 2020", "Type", "BU"],
    "2": ["N/A", "N/A", "N/A"],
    "3": ["N/A", "N/A", "N/A"],
    "4": ["test", "IR", "N/A"],
    "5": ["Total", "N/A", "N/A"]
  }
}
```

## Read Excel file by columns

Make a call to `/api/v1/read/columns` route to read each columns of a given file.

An input file need to be sent during the POST method. Only multipart file data are acceptable as input.

For example:

```bash
curl -F file=@testFiles/input.xlsx http://localhost:8000/api/v1/read/columns --output myFile.json
```

This API route read each columns of a given spreadsheet file and return a JSON with all values inside the file.

Example return value:

```javascript
{
  "Suivi charge": {
    "1": ["févr. 2020", "N/A", "N/A", "test", "Total"],
    "2": ["Type", "N/A", "N/A", "IR", "N/A"],
    "3": ["BU", "N/A", "N/A", "N/A", "N/A"]
  }
}
```

## Options

If your excel file contains some sheets and you only need to extract one of them, or you need to specify some coordinates for the beginning of reading, you can pass an options parameters that take a json value like that

```
{"options" : [{"sheet_name":"Feuil2", "starting_coordinates":"B2"}, {"sheet_name":"Feuil4"}]}
```

```bash
curl -F file=@testFiles/input.xlsx options='[{"sheet_name":"Feuil2", "starting_coordinates":"B2"}, {"sheet_name":"Feuil4"}]' http://localhost:8000/api/v1/read/columns --output myFile.json
```
