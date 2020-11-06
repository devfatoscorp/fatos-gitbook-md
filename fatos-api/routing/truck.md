---
description: Routing plan optimized for truck
---

# Route for truck

The Routing API will show you how to get where you’re going.   
With the Routing API, you can:

* Provide precise instructions to a destination using routing plans for various types of trucks
* To request directions, call four values: a start point, destination, and car type, and waypoint \(optional\).

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/fatos/api/route/truck" %}
{% api-method-summary %}
Routing API for truck
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="origin" type="string" required=true %}
Start point \(lat, lng\)
{% endapi-method-parameter %}

{% api-method-parameter name="destination" type="string" required=true %}
End point \(lat, lng\)
{% endapi-method-parameter %}

{% api-method-parameter name="key" type="string" required=true %}
Your API Key
{% endapi-method-parameter %}

{% api-method-parameter name="via" type="number" required=false %}
Waypoint \(lat, lng\), In the case of multiple waypoints, list them in order in the query string.
{% endapi-method-parameter %}

{% api-method-parameter name="car" type="integer" required=false %}
car type   
4. Heavy truck  
5. Very heavy truck  
7. Tank lorry  
8. Freight vehicle  
9. Construction vehicle
{% endapi-method-parameter %}

{% api-method-parameter name="rpoption" type="integer" required=false %}
Routing Plan Option  
Sum of each option value.  
1: Recommended 1  
2: Recommended 2  
4: Highway Priority  
8: General road Priority  
16: Shortest Distance  
32: Free road \(in the shortest time\)  
64: Exclude Car-only  
256: Free road \(in the shortest distance\)  
  
ex\) rpoption 3 =&gt; Recommended 1 + Recommended 2  
{% endapi-method-parameter %}

{% api-method-parameter name="angle" type="number" required=false %}
degrees \(0~359\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="warning" %}
**Display of Directions Results**

After you receive the requested results, you must decode the result into a geometry code. Call the Fatos.polyLine\(\) function as the decoded result and display the result on the map.
{% endhint %}

