---
description: Marker manipulation
---

# Marker

### Marker

Creates a marker on the map using the specified option. To display markers, you can set coordinate value, marker icons, and icon sizes.

```javascript
new fatosmap.maps.Marker({ option });
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| position | Latitude and longitude {lat, lng} | JSON |
| map | Map object to display the marker | Map instance |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Optional Parameter</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">icon</td>
      <td style="text-align:left">Sets the image of a marker</td>
      <td style="text-align:left">URL</td>
    </tr>
    <tr>
      <td style="text-align:left">iconSize</td>
      <td style="text-align:left">
        <p>Sets the size of a marker icon.</p>
        <p>The default is FATOS Bus Icon.</p>
      </td>
      <td style="text-align:left">
        <p>Numeric</p>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">message</td>
      <td style="text-align:left">Sets the popup message</td>
      <td style="text-align:left">String</td>
    </tr>
    <tr>
      <td style="text-align:left">anchor (popup)</td>
      <td style="text-align:left">A string indicating the part of the Marker that should be positioned closest
        to the coordinate set via Marker#setLngLat. Options are &apos;center&apos;
        , &apos;top&apos; , &apos;bottom&apos; , &apos;left&apos; , &apos;right&apos;.</td>
      <td
      style="text-align:left">String</td>
    </tr>
    <tr>
      <td style="text-align:left">offset (popup)</td>
      <td style="text-align:left">The offset in pixels as a PointLike object to apply relative to the element&apos;s
        center. Negatives indicate left and up. default 15</td>
      <td style="text-align:left">Numeric</td>
    </tr>
    <tr>
      <td style="text-align:left">closeButton (popup)</td>
      <td style="text-align:left">If true, a close button will appear in the top right corner of the popup.
        default false</td>
      <td style="text-align:left">Bool</td>
    </tr>
    <tr>
      <td style="text-align:left">closeOnClick (popup)</td>
      <td style="text-align:left">If true, the popup will be closed when the map is clicked. default false</td>
      <td
      style="text-align:left">Bool</td>
    </tr>
    <tr>
      <td style="text-align:left">addMarkerEvent</td>
      <td style="text-align:left">You can give the marker a promised event. (dragstart/drag/dragend)</td>
      <td
      style="text-align:left">JSON Array</td>
    </tr>
    <tr>
      <td style="text-align:left">drag</td>
      <td style="text-align:left">A boolean indicating whether or not a marker is able to be dragged to
        a new position on the map.</td>
      <td style="text-align:left">Bool</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
anchor, offset, closeButton, and closeOnClick are available only if the popup message is set. 
{% endhint %}

#### Example

```javascript
** Single Create Marker **
let marker = new fatosmap.maps.Marker({
        position: {lat: 37.5651745 , lng: 126.9858103 },
        map: mapInstance,
        icon: image(My Image),
        message: 'Fatos',
        anchor : 'bottom',
        offset : 15,
        closeButton: true,
        closeOnClick: true,
        drag: true,
        addMarkerEvent: [ {event:event name, callback function ()} ]
});

** Multi Create Markers **
let markers = []
let count = markers.length
let positions = [
        { lat: 37.564952 , lng: 125.987321 },
        { lat: 37.564952 , lng: 126.987321 },
        { lat: 37.564952 , lng: 124.987321 }
]

for(let i = 0; i < count; i++){
        let marker = new fatosmap.maps.Marker({
                position: positions[i],
                map: mapInstance
        })
        markers.push(marker)
        markers[i].setMap(mapInstance)
    }
```

#### RemoveMarker

Clears the markers shown on the map.

#### Example

```javascript
marker.setMap(null);
```

