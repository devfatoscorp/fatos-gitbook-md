# Language

### setLanguage

Sets the language of the map.

```text
mapInstance.setLanguage(language);
```

#### Parameter

| Required Parameter | Description | Type |
| :--- | :--- | :--- |
| language | specifies the language of the map. \("national" or "en"\) | String |

{% hint style="success" %}
"national" will display each region of the map with corresponding native language.
{% endhint %}

#### Example

```javascript
mapInstance.setLanguage("national");
```

### getLanguage

Retrieves the language parameter of the map instance.

```javascript
mapInstance.getLanguage();

return: "national"
```

