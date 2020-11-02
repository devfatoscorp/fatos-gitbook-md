---
description: Generate a circle and edit properties
---

# Circle

### Circle

Creates a circle that takes center point, radius, colors, and transparency as arguments.

```text
new fatosmap.maps.Circle({ option });
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| center | center point in latitude/longitude | JSON |
| radius | specifies the radius of the circle in meter | Numeric |

| Optional Parameter | Description | Type |
| :--- | :--- | :--- |
| fillColor | specifies a hexadecimal HTML color of the format "\#FFFFFF".The Circle class does not support named colors. The default is '\#000000' | Hex \(String\) |
| fillOpacity | specifies a numerical value between 0.0 and 1.0 to determine the opacity of the fill's color. The default is 1.0 | Numeric |
| text | Optional formatted. The defaults is "" | String |
| textColor | Optional color. Defaults to "\#000000". Requires "text" option. | Hex \(String\) |
| textHaloColor | Optional color. Defaults to "rgba\(0, 0, 0, 0\)". Requires "text" option. | RGBA |
| textHaloWidth | Optional number greater than or equal to 0. Units in pixels. Defaults to 0. Requires "text" option. | Numeric |
| textSize | Optional number greater than or equal to 0. Units in pixels. Defaults to 16. Requires "text" option. | Numeric |
| textOffset | Optional array of numbers. Units in ems. Defaults to \[0,0\]. Requires "text" option. | Numeric Array |

#### Example

```javascript
let center = {lat: 37.5650745, lng:126.9850103}

let cityCircle = new fatosmap.maps.Circle({	
    fillColor: '#FF0000',	
    fillOpacity: 0.35,	
    center: center,
    radius:10*100
    text: 'FATOS',
    textColor:'#fff',
    textSize: 25,
    textOffset:[5,4]
    textHaloWidth:10
});	
	
cityCircle.setMap(mapInstance);
```



