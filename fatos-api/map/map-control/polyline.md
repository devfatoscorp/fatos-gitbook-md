---
description: Connect vertices with lines
---

# Polyline

### Polyline

Sets latitude/longitude, color, transparency, line thickness. Draws a line on the map by combining the set value. Collects the values of multiple coordinates and express them as lines.

```javascript
new fatosmap.maps.Polyline({ option })
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| path | Each {lat, lng} behaves as a node | JSON Array |

| Optional Parameter | Description | Type |
| :--- | :--- | :--- |
| strokeColor | specifies a hexadecimal HTML color of the format "\#FFFFFF", The default is '\#000000' | Hex |
| strokeOpacity | specifies a numerical value between 0.0 and 1.0 to determine the opacity of the line's color. The default is 1.0 | Numeric |
| strokeWeight | specifies the width of the line in pixels. The default is 1 | Numeric |
| message \(popup\) | Set the message of popup, type is string or HTML | String / HTML |
| event | popup mouse event click or mouseover. The default click | String |
| anchor \(popup\) | A string indicating the part of the Marker that should be positioned closest to the coordinate set via Marker\#setLngLat. Options are 'center' , 'top' , 'bottom' , 'left' , 'right'. The default is bottom | String |
| offset \(popup\) | The offset in pixels as a PointLike object to apply relative to the element's center. Negatives indicate left and up. default 15 | Numeric |
| closeButton \(popup\) | If true, a close button will appear in the top right corner of the popup. The default is false | Bool |
| coloseOnClick \(popup\) | If true, the popup closes when the map is clicked. The default is false | Bool |

#### Example

```javascript
let line = [	
    {lat: 37.772, lng: -122.214},	
    {lat: 21.291, lng: -157.821},	
    {lat: -18.142, lng: 178.431},	
    {lat: -27.467, lng: 153.027}	
];	
let polyline = new fatosmap.maps.Polyline({	
    path:            line,                 	
    strokeColor:     '#0000FF',     	
    strokeOpacity:   0.5,       	
    strokeWeight:    10,
    message:         'FATOS',
    anchor:          'bottom',
    offset:          15,
    closeButton:     true,
    closeOnClick:    true,            	
});	
	
polyline.setMap(mapInstance);
```

### How to clear the polyline

Clears the path drawn on the map.

#### Example

```javascript
polyline.setMap(null);
```

#### 



