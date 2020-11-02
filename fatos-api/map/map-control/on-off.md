---
description: Event detection
---

# On/Off

### on / off

Adds or removes a listener for a specific event on a given layer.

```text
// Adds a listener
map.on(type, layerId, listener);

// Removes a listener
map.off(type, layerId, listener);
```

#### Parameter

| Parameter | Description | Type |
| :--- | :--- | :--- |
| type | specifies which event to listen to. | String |
| _Supported types:_ | "mouseup", "mousedown", "click", "dblclick", "mousemove", "mouseenter", "mouseleave, "mouseover", "mouseout", "contextmenu", "touchstart", touchend" or "touchcancel".  "mouseenter" and "mouseover" events are triggered when the cursor enters a visible portion of the specified layer or map canvas from outside and vice versa for "mouseleave" and "mouseout". |  |
| layerId \(Optional\) | ID of a style layer. Only layer that matches the given parameter will trigger the event listener. | String |
| listener | A callback function that detects the event and triggers further procedures. | Function |

#### Example

```javascript
// Event listener on click
map.on("click", function (e) {
    console.log("Click >>>>>>>", e)  
})

// Event listener on mouseover
map.on("mouseover", "fatosmarker", function (e) P
    if(e.originalEvent.toElement.id){
       console.log("Mouseover>>>>>>>", e)
    }
})

// Removes an event listener on click
map.off("click", function (e) {
    console.log("Click >>>>>>>", e)  
})

// Removes an event listener on mouseover
map.off("mouseover", "fatosmarker", function (e) P
    if(e.originalEvent.toElement.id){
       console.log("Mouseover>>>>>>>", e)
    }
})
```

