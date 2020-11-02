---
description: 'Search by POI such as airports, parks, mines, or gas station'
---

# POI

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/onemap/api/search/POI" %}
{% api-method-summary %}
POI Search
{% endapi-method-summary %}

{% api-method-description %}
Returns search results based on POI search queries and coordinate settings.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="kwd" type="string" required=true %}
Name search: search word  
Nearby search:  
category ID \(String to hex encoding\)  
  
i.e. {ABC Market} to {ec9db4eba788ed8ab8}
{% endapi-method-parameter %}

{% api-method-parameter name="stype" type="string" required=true %}
Search type  
Name search: 1  
Nearby search: 3
{% endapi-method-parameter %}

{% api-method-parameter name="cx" type="string" required=true %}
User's current location X coordinate \(wgs84\)
{% endapi-method-parameter %}

{% api-method-parameter name="cy" type="string" required=true %}
User's current location Y coordinate \(wgs84\)
{% endapi-method-parameter %}

{% api-method-parameter name="rad" type="string" required=true %}
Search radius \(Optional for name search\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
 “pgno”:,  page number
 “cnt”:, the number of searches
 “items”: lists of POI search results
 [
  {"id":, poi id
   "name""", POI expression name
   "addr1":"", new address
   "addr2":"", old address
   "phone":"", phone number : separator(,)
   "cate":"", classification code
   "posx":, poi x (longitude wgs84)
   "posy":, poi x (latitude wgs84)
   "entx":, poi entry point X (longitude wgs84)
   "enty":, poi entry point Y (latitude wgs84)
   "dist": distance(meter)
  },
 ]
} 
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

