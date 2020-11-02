---
description: Convert addresses into geographic coordinates
---

# Forward

Forward geocoding uses address information to return the coordinates of the area as a coordinate list of polygons.

{% hint style="info" %}
See the [**API Key Issuance page**](../../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/fatos/api/geocoding/forward" %}
{% api-method-summary %}
Forward Geocoding
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="format" type="string" required=true %}
\[ xml \| json \], output type methods.
{% endapi-method-parameter %}

{% api-method-parameter name="q" type="string" required=true %}
String to search with a keyword. A comma as a delimiter is optional but recommended for performance improvement.
{% endapi-method-parameter %}

{% api-method-parameter name="q\(Korean\)" type="string" required=true %}
Used when the keyword is Korean.
{% endapi-method-parameter %}

{% api-method-parameter name="polygon" type="integer" required=false %}
\[ 1 \| 0 \] Display the retrieved items or not. 
{% endapi-method-parameter %}

{% api-method-parameter name="addressdetails" type="integer" required=false %}
\[ 1 \| 0 \] Whether to separate addresses into details.
{% endapi-method-parameter %}

{% api-method-parameter name="acceptlanguage" type="string" required=false %}
countrycode\[,countrycode\]\[,countrycode\] Limit search results to specific countries. \(sg: singapore, th: thailand, id: indonesia, kr: korea, us: united states....\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "address_type": "way",
    "boundingbox": ["1.2783626", "1.2785892", "103.8029343", "103.8030164"],
    "polygonpoints": [["103.8029343", "1.2783626"], ["103.8030164", "1.2785892"]],
    "lat": "1.2783626",
    "lon": "103.8029343",
    "display_name":
      "Alexandra Road, Alexandra, Sentosa Cove, Southwest, 119578, Singapore",
    "class": "highway",
    "type": "primary",
    "importance": 0.30000000000000004,
    "address": {
      "road": "Alexandra Road",
      "hamlet": "Sentosa Cove",
      "county": "Southwest",
      "suburb": "Alexandra",
      "postcode": "119578",
      "country": "Singapore",
      "country_code": "sg"
    }
};
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Either one of "q" or "q\(Korean\)" parameters should be used.
{% endhint %}

