### Write a chart

To write a chart, you need to create an items array that contain a table and chart objects.
In fact, table object have all dataset used by chart.
Then, chart object contain all chart settings.

```json
"chart": {
  "type": "",
  "series": [{
    "name": "",
    "categories": "",
    "values": ""
  }],
  "format": {
    "x_scale": 1.0,
    "y_scale": 1.0,
    "x_offset": 15,
    "y_offset": 10,
    "print_obj": true,
    "lock_aspect_ratio": false,
    "locked": false
  },
  "legend": {
    "position": "left",
    "show_legend_key": false
  },
  "title":{
    "name": ""
  },
  "dimension": {
    "width":180,
    "height": 200
  },
  "plot_area": {
    "show_bubble_size": true,
    "show_cat_name": false,
    "show_leader_lines": false,
    "show_percent": true,
    "show_series_name": true,
    "show_val": true
  }
}
```

Type represent chart type

| type | | |
| ----------- | ----------- | ----------- |
| areaStacked | areaPercentStacked | area3D
| area3DStacked | area3DPercentStacked | bar
| barStacked | barPercentStacked | bar3DClustered
| bar3DStacked | bar3DPercentStacked | bar3DConeClustered
| bar3DConeStacked | bar3DConePercentStacked | bar3DPyramidClustered
| bar3DPyramidStacked | bar3DPyramidPercentStacked | bar3DCylinderClustered
| bar3DCylinderStacked | bar3DCylinderPercentStacked | col
| colStacked | colPercentStacked | col3DClustered
| col3D | col3DStacked | col3DPercentStacked
| col3DCone | col3DConeClustered | col3DConeStacked
| col3DConePercentStacked | col3DPyramid | col3DPyramidClustered
| col3DPyramidStacked | col3DPyramidPercentStacked | col3DCylinder
| col3DCylinderClustered | col3DCylinderStacked | col3DCylinderPercentStacked
| doughnut | line | pie
| pie3D | radar | scatter
| surface3D | wireframeSurface3D | wireframeContour
| contour | bubble | bubble3D


Series represent chart data

```json
{
  "series":[{
    "name": "",
    "categories": "",
    "values": ""
  }]
}
```

- ```name ```is series name
- ```categories ```is categories name
- ```values ``` is series values
