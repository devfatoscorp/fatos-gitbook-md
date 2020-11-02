---
description: Find a location by an address
---

# Address

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/fatos/api/search/ADDR" %}
{% api-method-summary %}
Address
{% endapi-method-summary %}

{% api-method-description %}
Returns search results based on address search queries and coordinate settings
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="kwd" type="string" required=true %}
Search word \(string to hex encoding\)  
{Ogeumno182} to {ec98a4eab888eba19c313832}
{% endapi-method-parameter %}

{% api-method-parameter name="stype" type="string" required=true %}
Search type: 2 \(for address search\)
{% endapi-method-parameter %}

{% api-method-parameter name="cx" type="string" required=true %}
User's current location X coordinate \(wgs84\)
{% endapi-method-parameter %}

{% api-method-parameter name="cy" type="string" required=true %}
User's current location Y coordinate \(wgs84\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{  
   "pano":,                       // page number
   "cnt":,                        // the number of searches
   "items":                       // list of POI search results
   [
       {   
          "id":,                         // poi id
          "name":"",                     // poi expression name
          "addr1":"",                    // new address
          "addr2":"",                    // old address
          "phone":"", 
          "phone number":                // separator (,)
          "cate":"",                     // classification code
          "posx":"",                     // poi x (longitude wgs84)
          "posy":"",                     // poi y (latitude wgs84)
          "entx":"",                     // poi entry point x (longitude wgs84)
          "enty":"",                     // poi entry point y (latitude wgs84)
          "dist":                        // distance(meter)
       },
   ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

