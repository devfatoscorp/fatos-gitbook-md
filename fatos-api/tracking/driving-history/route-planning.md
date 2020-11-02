---
description: In depth routing plan instructions
---

# Routing Plan

{% hint style="info" %}
See the [**API Key Issuance page**](../../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/mobilizer/route" %}
{% api-method-summary %}
Routing Plan
{% endapi-method-summary %}

{% api-method-description %}
Retrieves the routing plan data such as travel mode and navigation instruction.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="uuid" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="gid" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "uuid": "UUID",
    "gid": "1579148696652",
    "utime": "2020-01-16 04:24:56",
    "geom": [
      [
        126.4575804,
        37.441513,
-1
      ],
      [
        126.5637816,
        37.4898376,
-1
      ]
    ],
    "rp_order":1,
    "route": {
      "copyrights": "지도 데이터 ©2019 FATOS Co,. Ltd",
      "bounds": {
        "northeast": {
          "lat": 37.489700224735685,
          "lng": 126.56550775820193
        },
        "southwest": {
          "lat": 37.43994894301858,
          "lng": 126.44935308753611
        }
      },
      "legs": {
        "distance": 17728,
        "duration": 0,
        "start_address": "",
        "start_location": {
          "lng": 126.45754133521325,
          "lat": 37.441492941736186
        },
        "end_address": "",
        "end_location": {
          "lng": 126.56367765718954,
          "lat": 37.489700224735685
        },
        "traffic_speed_entry": [],
        "via_waypoint": [],
        "stpes": [
          {
            "attr": 279470337,
            "distance": 25,
            "duration": 0,
            "start_location": {
              "lng": 126.45754133521325,
              "lat": 37.441492941736186
            },
            "end_location": {
              "lng": 126.45741640387786,
              "lat": 37.4412735966435
            },
            "maneuver": "직진",
            "html_instructions": "영종해안남로321번길||제1여객터미널|제1여객터미널||영종해안남로321번길",
            "laneguide": "",
            "polyline": {
              "points": "aXxmbGZBaWtqZXBGcEFQZEJqQH5GekQ=",
              "mbr": {
                "minx": 126.45741640387786,
                "miny": 37.4412735966435,
                "maxx": 126.45754133521325,
                "maxy": 37.441492941736186
              }
            },
            "travel_mode": "DRIVING"
          },
...omit...
    {
            "attr": 271074049,
            "distance": 200,
            "duration": 0,
            "start_location": {
              "lng": 126.56544958406869,
              "lat": 37.4885396030931
            },
            "end_location": {
              "lng": 126.56367765718954,
              "lat": 37.489700224735685
            },
            "maneuver": "직진",
            "html_instructions": "하늘별빛로|||||",
            "laneguide": "",
            "polyline": {
              "points": "d3hib2ZBc2N9a3BGe0R+R2VtQHplQXNDYEZlQm5Dc0tmUg==",
              "mbr": {
                "minx": 126.56367765718954,
                "miny": 37.4885396030931,
                "maxx": 126.56544958406869,
                "maxy": 37.489700224735685
              }
            },
            "travel_mode": "DRIVING"
          }
        ]
      },
      "overview_polyline": {
        "point": ""
      },
      "summary": "공항로|하늘대로|영종대로",
      "warnings": "",
      "waypoint_order": []
    }
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

