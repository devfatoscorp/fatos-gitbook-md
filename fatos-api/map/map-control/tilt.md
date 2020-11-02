---
description: Tilt your 3d map view
---

# Tilt

### setTilt

Sets the slope/tilt of the map view. The parameter ranges from 0 to 60. If the value is closer to 0, then the map appears to be 2D. If the value is close to 60, the map appears to be 3D.

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| value | Slope | Numeric \(0-60\) |

### Example

```text
mapInstance.setTilt(40);
```

### getTilt

Gets the slope/tilt value of the map.

#### Return

The current tilt of the map.

#### Example

```javascript
mapInstance.getTilt();
return 40
```

