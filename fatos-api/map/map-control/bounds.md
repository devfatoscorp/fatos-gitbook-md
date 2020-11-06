---
description: Bounds for map viewport
---

# Bounds

### fitBounds

takes bounds and opt as arguments and sets the center of the map with the given parameter. bounds parameter is a JSON object with two intercardinal directions \(sw and ne\), with latitude and longitude \(lat, lng\) respectively.

```javascript
mapInstance.fitBounds(bounds, opt);
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| bounds | Center these bounds in the viewport and use the highest zoom level up to and including the map. | JSON |

| Optional Parameter | Description | Type |
| :--- | :--- | :--- |
| padding | The amount of padding in pixels to add to the given bounds. | Numeric |
| linear | If true, the map transitions using Map\#easeTo. If false, the map transitions using Map\#flyTo. | Bool |
| maxZoom | The maximum zoom level to allow when the map view transitions to the specified bounds. | Numeric |

#### Example

```javascript
let bounds = {
        sw: {lat: 37.457464, lng: 126.899302},
        ne: {lat: 37.645804, lng: 127.161728}
}

let opt = {
	padding: {
           top: 5,
           bottom: 5,
           right: 15,
           left: 15
	},
	linear: true, 	    // true for “easeTo” false for “flyTo”
	maxZoom: 10
}

let opt2 = {
	padding: 10	        // 10 for top, bottom, right, and left.
}

mapInstance.fitBounds(fit, opt);
mapInstance2.fitBounds(fit, opt2);


```

### getBounds

Retrieves the bounds attribute set in 'fitBounds\(\)'

```javascript
mapInstance.getBounds();
```

#### Return

Intercardinal coordinates \(ne, sw\) with latitude and longitude

```javascript
mapInstance.getBounds();
return : {
        ne : {lat: 37.645804, lng: 127.161728}
        sw : {lat: 37.457464, lng: 126.899302}
}
```



