---
description: Edit button properties
---

# Button control

### Button Visibility

You can toggle the visibility of control buttons with the following functions.

```javascript
/*
You can create or remove a button bar at the top right of 
the map with all buttons.
*/
mapInstance.onBtnAll();
mapInstance.offBtnAll();

// Zoom-in and zoom-out button.
mapInstance.onBtnZoom();
mapInstance.offBtnZoom();

// Compass button.
mapInstance.onBtnCompass();
mapInstance.offBtnCompass();

// Pitch button.
mapInstance.onBtnPitch();
mapInstance.offBtnPitch();

// Satellite button.
mapInstance.onBtnSatellite();
mapInstance.offBtnSatellite();

// Bering button.
mapInstance.onBtnBering();
mapInstance.offBtnBering();

// Full-screen button.
mapInstance.onBtnFullScreen();
mapInstance.offBtnFullScreen();

// Geographic location button.
mapInstance.onBtnGeoLocate();
mapInstance.offBtnGeoLocate();
```



