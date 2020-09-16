# Writer

## Write an excel file

To create an excel file with Excelante, you need to call the API `/api/v1/write` with POST method and pass the following json scheme to the route. Some fiedls are optionnal, feel free to use it or not.

```json
{
  "sheets": [{                                // Array of sheets
    "name": "Sheet1",                         // Name of the sheet
    "orientation": "OrientationLanscape",     // (Optionnal) Is the orientation of layout. (OrientationPortrait || OrientationLanscape) Default is set to OrientationPortrait.
    "items": [{                               // Array of items. An item is an object that can be write into excel file.
      "starting_cell_coordinates": "B3",      // (Optionnal) Represent the begining coordonates of the item.
      "table": [{                            // Array of data. Represent all data of an excel table that can be write into file. An object of tables is write by column or by row
        "orientation": "column",              // Represent the mode of writing. (column || row)
        "cells": [{                           // Represent an array of cells to wwrite
          "value": "myValue",                 // Value of the cell
          "style": {                          // (Optionnal) Describe the style of the cell
            "border": [{                      // (Optionnal) Describe all the border of the cell.
              "type": "top",                  // Type is the position of border. Can be (top || bottom || left || right)
              "color": "#000000",             // Color is the border color.
              "style":1                       // Style is the border format (See border style reference)
            }],
            "fill": {                          // (Optionnal) Represent cell fill
              "type": "pattern",              // Type of fill
              "color": ["#87CEFA"],           // Fill color
              "pattern": 1,                   // Fill pattern (See fill style reference)
              "shading":1                     // (Optionnal) Shading fill (See fill style reference)
            },
            "font": {                         // (Optionnal) Represent cell text font
              "bold": true,                   // (Optionnal) Bold (true) or not (false)
              "italic": true,                 // (Optionnal) Italic (true) or not (false)
              "underline": "single",          // (Optionnal) Underline text (See font style reference)
              "family": "Times New Roman",    // (Optionnal) Family of font
              "size": 14.5,                   // (Optionnal) Size of font
              "strike": true,                 // (Optionnal) Strike (true) or not (false)
              "color": "#000000"              // (Optionnal) Color of font
            },
            "alignment": {                    // (Optionnal) Represent cell content aligment
              "horizontal":"center",          // (Optionnal) Represent horizontal alignment into the cell (See alignment style reference)
              "vertical": "top",              // (Optionnal) Represent vertical alignment into the cell (See alignment style reference)
              "shrink_to_fit": true,           // (Optionnal) Shrink to fit cell text
              "wrap_text": false              // (Optionnal) Wrap cell text
            },
            "protection": {                   // (Optionnal) Represent cell protection
              "hidden": 0,                    // (Optionnal) Cell is hidden (true) or not (false)
              "locked": 0                     // (Optionnal) Cell is locked (true) or not (false)
            }
          },
          "is_formula": true,                 // (Optionnal) Set true if the current cell value is a formula.
        }]
      }],
      "chart": {                              // (Optionnal) Represent a graph item
        "type": "bar",                        // Type of chart (See graph type reference)
        "series": [{                          // Array of data to draw the chart.
            "name": "Sheet1!$A$2",            // Name of the serie
            "categories": "Sheet1!$A$2",      // Category of the serie
            "values": "Sheet1!$B$2:$D$2"      // Value of the serie
        }],
        "format":{
            "x_scale": 1.0,                   // Set x scale for chart
            "y_scale": 1.0,                   // Set y scale for chart
            "x_offset": 15,                   // Set x offset for chart
            "y_offset": 10,                   // Set y offset for chart
            "print_obj": true,                //
            "lock_aspect_ratio": false,       // Lock x/y ratio
            "locked": false                   // Lock chart
        },
        "legend":{                            // (Optionnal) Legend of the graph
            "position": "left",               // Legend position (See legend graph reference)
            "show_legend_key": false          // Show legend but not overlap with chart
        },
        "title":{                             // Title of the graph
            "name": "Chart of my data"        // Name of chart
        },
        "dimension": {                        // Set graph dimension
            "height": 290,                    // Set height. Default 290
            "width": 480                      // Set width. Default 480
        },
        "plot_area":{                          // Set the position of the chart plot area
            "show_bubble_size": true,         // Specifies the bubble size shall be shown in a data label. Default false.
            "show_cat_name": false,           // Show category name. Default true.
            "show_leader_lines": false,       // Specifies that the category name shall be shown in the data label. Default false.
            "show_percent": true,             // Specifies that the percentage shall be shown in a data label. Default false.
            "show_series_name": true,         // Specifies that the series name shall be shown in a data label. Default false.
            "show_val": true                  // Specifies that the value shall be shown in a data label. Default false.
        }
      }
    }]
  }, {
    "name": "Sheet2",
    ...
  }]
}
```
