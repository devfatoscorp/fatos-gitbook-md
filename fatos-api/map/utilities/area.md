---
description: Get an area of given coordinates
---

# Area

### getArea

Returns the area in meter squared of a polygon.

```text
mapInstance.getArea(coordinates)
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| coordinates | Array of latitude/longitude. The array must contain at least 3 coordinates. | JSON Array |

#### Example

```javascript
mapInstance.getArea(
   [
       {lng: -122.019807, lat: 45.632433},
       {lng: -122.019767, lat: 45.632453},
       {lng: -122.01971, lat: 45.632472}
   ])
```

#### Return

Area value in meter squared

