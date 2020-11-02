---
description: Summary of each trip
---

# Tracking Summary

{% hint style="info" %}
See the [**API Key Issuance page**](../../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/mobilizer/drivehistory" %}
{% api-method-summary %}
Tracking Summary via driving history
{% endapi-method-summary %}

{% api-method-description %}
Gets the summary of the trip history of a unit, corresponding to the given date.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="uuid" type="string" required=true %}
UUID of the search target
{% endapi-method-parameter %}

{% api-method-parameter name="fdate" type="string" required=true %}
Start date \(YYYY-MM-DD\)
{% endapi-method-parameter %}

{% api-method-parameter name="tdate" type="string" required=true %}
End date \(YYYY-MM-DD\)
{% endapi-method-parameter %}

{% api-method-parameter name="mode" type="string" required=true %}
Fixed to default 0
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
    "gid": "1578039637949000",
    "start_time": "2020-01-03 07:20:30",
    "end_time": "2020-01-03 08:19:10",
    "sum_dist": 18144,
    "sum_time": 3296,
    "start_lon": 127.07844911845706,
    "start_lat": 37.511755850641805,
    "end_lon": 126.98550783431699,
    "end_lat": 37.51778497966757
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
| start\_time | Start time of the trip |
| end\_time | End time of the trip |
| sum\_dist | Total distance of the trip \(Meter\) |
| sum\_time | Total driving time of the trip\(Sec\) |
| start\_lon | The X coordinate of the first position of the trip |
| start\_lat | The Y coordinate of the first position of the trip |
| end\_lon | The X coordinate of the last position of the trip |
| end\_lat | The Y coordinate of the last position of the trip |

