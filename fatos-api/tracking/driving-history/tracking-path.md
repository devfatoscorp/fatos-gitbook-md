---
description: Find how you went to your destination
---

# Tracking Path

{% hint style="info" %}
See the [**API Key Issuance page**](../../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/mobilizer/drivehistory/pattern" %}
{% api-method-summary %}
Driving Pattern via driving history
{% endapi-method-summary %}

{% api-method-description %}
Retrieves data to display driver's driving patterns on a map
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key. 
{% endapi-method-parameter %}

{% api-method-parameter name="uuid" type="string" required=true %}
UUID of a search target
{% endapi-method-parameter %}

{% api-method-parameter name="gid" type="string" required=true %}
trip id
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
    "gid": "1578035717694000",
    "utime": "2020-01-03 06:15:30",
    "over_speed": 0,
    "rapid_acceleration": 0,
    "rapid_deceleration": 0,
    "quick_start": 1,
    "sudden_stop": 0,
    "rescan": 0,
    "sudden_spin": 0,
    "sudden_uturn": 0,
    "lon": 127.07408415111274,
    "lat": 37.50924768719074,
    "os_dist": 0,
    "os_time": "0",
    "os_speed": 0,
    "speed_limit": 30,
    "level": "1"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



#### Return

| Parameter | Description |
| :--- | :--- |
| uuid | UUID of the user |
| gid | Trip ID |
| utime | Event time \(YYYY-MM-DD HH24:MI:SS\) |
| over\_speed | Speeding \(0: not speeding, 1: over speeding\) |
| rapid\_acceleration | Sudden acceleration |
| rapid\_deceleration | Sudden deceleration |
| quick\_start | Sudden departure |
| sudden\_stop | Sudden stop |
| rescan | Whether to rescan |
| sudden\_spin | Rapid turn |
| sudden\_uturn | Rapid u-turn |
| lon | X coordinate |
| lat | Y coordinate |
| os\_dist | Overspeed mileage |
| os\_time | Overspeed time |
| os\_speed | Overspeed |
| speed\_limit | Speed limit |
| level | Determine pattern marker display according to map scale level: 1 &gt; from level 9 level: 2 &gt; from level 13 level: 3 &gt; from level 16 level: 4 &gt; from level 18 |

