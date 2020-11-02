---
description: Animated focus to a location
---

# Flyto

### flyTo

Takes a JSON object as a parameter that contains latitude, longitude, zoom, and optional speed. Displays a location that matches the parameters with flying animation. 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">lat</td>
      <td style="text-align:left">Latitude</td>
      <td style="text-align:left">Numeric</td>
    </tr>
    <tr>
      <td style="text-align:left">lng</td>
      <td style="text-align:left">Longitude</td>
      <td style="text-align:left">Numeric</td>
    </tr>
    <tr>
      <td style="text-align:left">zoom</td>
      <td style="text-align:left">Zoom level of the map</td>
      <td style="text-align:left">Numeric</td>
    </tr>
    <tr>
      <td style="text-align:left">speed (optional)</td>
      <td style="text-align:left">
        <p>Determines flying animation speed</p>
        <p>The default value: 2.5</p>
      </td>
      <td style="text-align:left">Numeric</td>
    </tr>
  </tbody>
</table>

#### Example

```javascript
mapInstance.flyTo ({
    lat: 37.553749,
    lng: 126.808706,
    zoom: 15,
    speed: 4
})
```

