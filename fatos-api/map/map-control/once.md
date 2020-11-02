---
description: Event detection
---

# Once

### once

Adds a one-time listener for an initial occurrence of a specific event on a given layer.

```javascript
map.once(type, layerId, listener);
```

#### Parameter

{% hint style="info" %}
Parameters for "once" is same as "on" or "off" function.
{% endhint %}

{% page-ref page="on-off.md" %}

#### Example

```javascript
// Event listener once click
map.once("click", function (e) {
    console.log("Click >>>>>>>", e)  
})

// Event listener once mouseover
map.once("mouseover", "fatosmarker", function (e) P
    if(e.originalEvent.toElement.id){
       console.log("Mouseover>>>>>>>", e)
    }
})
```



