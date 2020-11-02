---
description: Fill colors the area within given vertices
---

# Polygon

### Polygon

Creates a custom polygon. Takes JSON Array of at least 3 latitude/longitude for vertices, color, and transparency as arguments.

```javascript
new fatosmap.maps.Polygon({ option });
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| paths | Coordinate value for each vertex | JSON Array |

| Optional Parameter | Description | Type |
| :--- | :--- | :--- |
| fillColor | specifies a hexadecimal HTML color of the format "\#FFFFFF". The Polygon class does not support named colors. The default is '\#000000' | Hex \(String\) |
| fillOpacity | specifies a numerical value between 0.0 and 1.0 to determine the opacity of the fill's color. The default is 1.0 | Numeric |
| outlineColor | specifies a hexadecimal HTML outline color of the format "\#FFFFFF". The Polygon class does not support named colors. The default is '\#000000' | Hex \(String\) |
| text | Optional formatted. Defaults to "" | String |
| textColor | Optional color. Defaults to "\#000000". Requires "text" option. | Hex \(String\) |
| textHaloColor | Optional color. Defaults to "rgba\(0, 0, 0, 0\)". Requires "text" option. | RGBA |
| textHaloWidth | Optional number greater than or equal to 0. Units in pixels. Defaults to 0. Requires "text" option. | Numeric |
| textSize | Optional number greater than or equal to 0. Units in pixels. Defaults to 16. Requires "text" option. | Numeric |
| textOffset | Optional array of numbers. Units in ems. Defaults to \[0,0\]. Requires "text" option. | Numeric Array |

#### Example

```javascript
let triangleCoords = [	
    {lat: 25.774, lng: -80.190},	
    {lat: 18.466, lng: -66.118},	
    {lat: 32.321, lng: -64.757},	
    {lat: 25.774, lng: -80.190}	
];	
	
let polygons = new fatosmap.maps.Polygon({	
    paths:             triangleCoords,	
    fillColor:         '#FF0000',	
    fillOpacity:       0.35,
    outlineColor:      '#DC151A',
    text:              'FATOS',
    textColor:         '#91FF7C',
    textSize:          25,
    textOffset:        [5,4],
    textHaloWidth:     10	
});	
	
bermudaTriangle.setMap(mapInstance);
```

### How to remove polygons

Clears the polygon drawn on the map

#### Example

```javascript
// Method 1.
bermudaTriangle.setMap(null);

// Method 2.
polygon.setMap("removeAll");
```

### setVisible

Sets a visibility option for a polygon instance.

#### Example

```javascript
polygon.setVisible("none");
```

### 

