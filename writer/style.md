### Write style

Style can be applied to a cell.

```json
"style": {
  "border": [{}],
  "fill": {},
  "font": {},
  "alignment": {},
  "protection": {}
}
```

Style contains the following fields :

- An array of ```border ```
- A ```fill ```object
- A ```font ```object
- An ```alignment ``` object
- A ```protection ``` object

#### Border reference

```json
"border": [{
  "type": "top",
  "color": "#000000",
  "style":1
}]
```

Type represent border position

| type |
| ----------- |
| top |
| bottom |
| left |
| right |

Style represent border style

| style | value |
| ----------- | ----------- |
| 0 | None
| 1 | Continuous
| 2 | Continuous with double lines
| 3 | Dash
| 4 | Dot
| 5 | Continuous with 3 lines
| 6 | Double
| 7 | Continuous with no line
| 8 | Dash with 2 lines
| 9 | Dash Dot
| 10 | Dash Dot with 2 lines
| 11 | Dash Dot Dot
| 12 | Dash Dot Dot with 2 lines
| 13 | SlantDash Dot

#### Fill reference

```json
"fill": {
  "type":"pattern",
  "color": "",
  "pattern": 1,
  "shading":1
}
```

| pattern |
| ---------- | ---------- | ---------- | ---------- |
| 0 | None | 10 | ![pattern10](../img/pattern_10.png)|
| 1 |  | 11 | ![pattern11](../img/pattern_11.png)|
| 2 | ![pattern2](../img/pattern_02.png)| 12 | ![pattern12](../img/pattern_12.png)|
| 3 | ![pattern3](../img/pattern_03.png)| 13 | ![pattern13](../img/pattern_13.png)|
| 4 | ![pattern4](../img/pattern_04.png)| 14 | ![pattern14](../img/pattern_14.png)|
| 5 | ![pattern5](../img/pattern_05.png)| 15 | ![pattern15](../img/pattern_15.png)|
| 6 | ![pattern6](../img/pattern_06.png)| 16 | ![pattern16](../img/pattern_16.png)|
| 7 | ![pattern7](../img/pattern_07.png)| 17 | ![pattern17](../img/pattern_17.png)|
| 8 | ![pattern8](../img/pattern_08.png)| 18 | ![pattern18](../img/pattern_18.png)|
| 9 | ![pattern9](../img/pattern_09.png)|

| shading |
| ---------- | ---------- |
| 0 | Horizontal
| 1 | Vertical
| 2 | Diagonal up
| 3 | Diagonal down
| 4 | From corner
| 5 | From center


#### Font reference

```json
"font": {
  "bold": true/false,
  "italic": true/false,
  "underline": "single",
  "family": "Times New Roman",
  "size": 14.5,
  "strike": true/false,
  "color": ""
}
```

| underligne |
| ------------- |
| single |
| double |

#### Alignment reference

```json
"alignment": {
  "horizontal":"",
  "vertical": "",
  "shrink_to_fit": true/false,
  "wrap_text": true/false
}
```

| horizontal |
| ------------- |
| left |
| center |
| right |
| fill |
| justify |
| centerContinous |
| distributed |


| vertical |
| ------------- |
| top |
| center |
| justify |
| distributed |


#### Protection reference

```json
"protection": {
  "hidden": true/false,
  "locked": true/false
}

```
