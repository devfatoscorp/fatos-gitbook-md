# Center

### setCenter

Sets the center of the map.

```text
mapInstance.setCenter(LatLng);
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| LatLng | Latitude and longitude to be set as the center of the map | JSON |

#### Example

```javascript
let LatLng = {
        lat: 37.574674, 
        lng: 126.958004
}
mapInstance.setCenter(LatLng);
```

### getCenter

Retrieves the latitude and longitude value set in "setCenter\(\)"

```javascript
mapInstance.getCenter();
```

#### Return

The map's geographical center point

#### Example

```javascript
mapInstance.getCenter();
return : {
        lat: 37.574674, 
        lng: 126.958004
}
```

