---
description: Focal point for rotating a map view
---

# Heading

### setHeading

Takes an angle value \(in degree\) and sets "heading" \(focal point\) to rotate the map in the desired direction or angle. The default is 0 degree \(North\)

```text
mapInstance.setHeading(value);
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| value | Angle in degree from 0 to 360 | Numeric |

#### Example

```text
mapInstance.setHeading(90);
```

### getHeading

Gets the current focal point \(heading\) value in angle.

```javascript
mapInstance.getHeading();
```

#### Return

The angle in degree.

#### Example

```javascript
mapInstance.getHeading();
return : 90
```

