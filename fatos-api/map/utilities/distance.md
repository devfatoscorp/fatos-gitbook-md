---
description: Get a distance for given coordinates
---

# Distance

### getDistance

Returns the distance in meter between 2 or more coordinates.

```javascript
mapInstance.getDistance(coordinates)
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| coordinates | Array of latitude/longitude. The array must contain at least 2 coordinates. | JSON Array |

#### Example

```javascript
mapInstance.getDistance(
   [
       {lng: -122.019807, lat: 45.632433},
       {lng: -122.019767, lat: 45.632453},
       {lng: -122.01971, lat: 45.632472}
   ])
```

#### Return

Distance value in the meter.

