---
description: Convert geographic coordinates into addresses
---

# Reverse

Reverse geocoding uses latitude and longitude information to provide an address. An optional description of the zoom level provides information suitable for the OpenLayers room level.

{% hint style="info" %}
See the [**API Key Issuance page**](../../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/search/v1/geocoding/reverse" %}
{% api-method-summary %}
Reverse Geocoding
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="cy" type="string" required=true %}
Y coordinate of the search target
{% endapi-method-parameter %}

{% api-method-parameter name="cx" type="string" required=true %}
X coordinate of the search target
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "lat": "1.27836263535848",
    "lon": "103.802934312811",
    "display_name":
      "Alexandra Road, Alexandra, Sentosa Cove, Southwest, 119578, Singapore",
    "address": {
      "road": "Alexandra Road",
      "county": "Southwest",
      "postcode": "119578",
      "country": "Singapore",
      "country_code": "sg"
    },
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

