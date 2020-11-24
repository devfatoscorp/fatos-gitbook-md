---
description: Flexible instructions to the destination
---

# Route

The Routing API will show you how to get where you’re going.   
With the Routing API, you can:

* Provide precise instructions to a destination using various transport modes \(e.g., car, public transit, bicycle\).
* To request directions, call four values: a start point, destination, and car type, and waypoint \(optional\).

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/fatos/api/route" %}
{% api-method-summary %}
Routing API
{% endapi-method-summary %}

{% api-method-description %}
​
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
1: compact  
2: standard  
3: full size  
6: minicompact
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
https://api.fatos.biz/fatos/api/route?key=Y OUR\_API\_KEY&origin=37.483294848898396,126.89654749206602&destination=37.51702306480502,127.0416190159097&angle=-1&rpoption=1&servicesvr=2&unixtime=1604626833&gmtoffset=32400&cartype=1
{% endapi-method-response-example-description %}

```javascript
{
  "routes": [
    {
      "rpoption": 1,
      "bounds": {
        "lefttop": {
          "lon": 127.006812,
          "lat": 36.081916
        },
        "rightbottom": {
          "lon": 128.36276,
          "lat": 37.560658
        }
      },
      "legs": [
        {
          "distance": {
            "text": "339.7 km",
            "value": 339760
          },
          "duration": {
            "text": "265 min",
            "value": 15909
          },
          "end_location": {
            "lon": 128.325439,
            "lat": 36.144195
          },
          "start_location": {
            "lon": 127.02298,
            "lat": 37.559692
          },
          "step": [
            {
              "distance": {
                "text": "0 m",
                "value": 0
              },
              "duration": {
                "text": "0 sec",
                "value": 0
              },
              "end_location": {
                "lon": 127.022793,
                "lat": 37.559661
              },
              "start_location": {
                "lon": 127.022793,
                "lat": 37.559661
              },
              "polyline": {
                "points": "{zfdFmchfW"
              },
              "instructions": "starting point",
              "roadcategory": 12,
              "maneuver": 49
            },
            {
              // steps omitted
            },
            {
              "distance": {
                "text": "0.1 km",
                "value": 116
              },
              "duration": {
                "text": "56 sec",
                "value": 56
              },
              "end_location": {
                "lon": 127.023163,
                "lat": 37.560658
              },
              "start_location": {
                "lon": 127.022793,
                "lat": 37.559661
              },
              "polyline": {
                "points": "{zfdFmchfWIEUS]YGEGCWA_BI"
              },
              "instructions": "Destination",
              "roadcategory": 12,
              "maneuver": 3
            }
          ],
          "via_waypoint": [
            {
              "location": {
                "lon": 127.123108,
                "lat": 36.123123
              },
              "step_index": 27
            }
          ]
        }
      ],
      "overview_polyline": {
        "points_count": 3986,
        "points": "{zfdFmchfW??IEUS]YGEGCWA_BI?wBtDCP@Z@lCJ`@C\\G`@ULMx@eARS...."
      }
    }
  ],
  "status": "OK"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="warning" %}
**Display of Directions Results**

After you receive the requested results, you must decode the result into a geometry code. Call the Fatos.polyLine\(\) function as the decoded result and display the result on the map.
{% endhint %}



