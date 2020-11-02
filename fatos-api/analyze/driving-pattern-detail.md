---
description: Detail data of your driving pattern
---

# Driving Pattern Detail

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/analysing/drivehistory/pattern" %}
{% api-method-summary %}
Driving Pattern Detail \(For a specific trip\)
{% endapi-method-summary %}

{% api-method-description %}
Returns detailed information on the driving pattern event marker displayed on the map.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="utime" type="string" required=true %}
Unix time of an event
{% endapi-method-parameter %}

{% api-method-parameter name="key" type="string" required=true %}
Your API Key. 
{% endapi-method-parameter %}

{% api-method-parameter name="uuid" type="string" required=true %}
UUID of a search target
{% endapi-method-parameter %}

{% api-method-parameter name="gid" type="string" required=true %}
Trip ID
{% endapi-method-parameter %}

{% api-method-parameter name="mode" type="string" required=true %}
Fixed to default 1
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
[
  {
    "uuid": "5725415894ec71cd",
    "gid": "1581308924807",
    "unixtime": "1581313606",
    "utime": "2020-02-10 14:46:46",
    "cur_speed": 26,
    "cur_angle": 209,
    "rapid_acceleration": null,
    "rapid_deceleration": 8,
    "quick_start": null,
    "emergency_stop": null,
    "sudden_spin": null,
    "sudden_uturn": null,
    "os_time": null,
    "os_dist": null,
    "os_speed": null,
    "speed_limit": 40
  }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



| Return Parameter | Description |
| :--- | :--- |
| uuid | UUID of the user |
| gid | Trip ID |
| utime | Trajectory time |
| status | status \(You don't need to use data that is currently rooted\) |
| score | score \(You don't need to use data that is currently rooted\) |
| road\_cate | Road category \(You don't need to use data that is currently rooted\) |
| link\_cate | Link category \(You don't need to use data that is currently rooted\) |
| link\_facil | Link facility \(You don't need to use data that is currently rooted\) |
| oneway | One way traffic \(You don't need to use data that is currently rooted\) |
| lane | lane \(You don't need to use data that is currently rooted\) |
| max\_speed | Speed limit |
| shadow\_area | Shaded area |
| lon | X coordinate of trajectory \(WGS84\) |
| lat | Y coordinate of trajectory \(WGS84\) |
| east | MBR \(northeast\) + \(southwest\) |
| west |  |
| north |  |
| south |  |
| level | Determine whether or not to show the trajectory according to the map scale level: 1 &gt; from level 9 level: 2 &gt; from level 13 level 3 &gt; from level 16 level 4 &gt; from level 18 |
| hacuracy | GPS accuracy 10 is less than the correct signal, More than 10, less accurate |

