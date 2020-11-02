---
description: Evaluation of your driving pattern
---

# Driving Pattern Statistics

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/analysing/drivepattern" %}
{% api-method-summary %}
Statistics for Drive Pattern
{% endapi-method-summary %}

{% api-method-description %}
Returns driving pattern statistics for driving score and speed chart.
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

{% api-method-parameter name="fdate" type="string" required=true %}
Start date \(YYYY-MM-DD\)
{% endapi-method-parameter %}

{% api-method-parameter name="tdate" type="string" required=true %}
End date \(YYYY-MM-DD\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "uuid": "22FD6815-AC7A-4E80-8104-DD2E94A4B21A",
    "over_speed": "20",
    "rapid_acceleration": "38",
    "rapid_acc_point": "0.0",
    "rapid_deceleration": "39",
    "rapid_dec_point": "0.0",
    "quick_start": "12",
    "quick_start_point": "3.0",
    "sudden_stop": "10",
    "sudden_stop_point": "3.0",
    "rescan": "0",
    "rescan_point": "5.0",
    "sudden_spin": "5",
    "sudden_spin_point": "4.0",
    "sudden_uturn": "0",
    "sudden_uturn_point": "5.0",
    "echo_time": "437",
    "idle_time": {
      "days": 16,
      "hours": 16,
      "minutes": 53,
      "seconds": 25,
      "milliseconds": 460.575
    },
    "sum_score": "65",
    "sum_dist": 9815,
    "sum_time": "561",
    "os_dist": 0,
    "os_time": "0",
    "os_speed": 0,
    "lon": 126.66835390378799,
    "lat": 37.56899633676244
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

| Return Parameter | Description |
| :--- | :--- |
| uuid | uuid of the user |
| over\_speed | speeding |
| rapid\_acceleration | Sudden acceleration |
| rapid\_acc\_point | Rapid acceleration rating \(0.0 ~ 5.0, 0.5unit\) |
| rapid\_deceleration | Rapid deceleration |
| rapid\_dec\_point | Rapid deceleration rating \(0.0 ~ 5.0, 0.5unit\) |
| quick\_start | quick start |
| quick\_start\_point | quick start rating \(0.0 ~ 5.0, 0.5unit\) |
| sudden\_stop | Sudden stop |
| sudden\_stop\_point | Sudden stop rating \(0.0 ~ 5.0, 0.5unit\) |
| rescan | rescan |
| rescan\_point | rescan rating \(0.0 ~ 5.0, 0.5unit\) |
| sudden\_spin | doubling |
| sudden\_spin\_point | doubling rating \(0.0 ~ 5.0, 0.5unit\) |
| sudden\_uturn | Rapid U-turn |
| sudden\_uturn\_point | Rapid U-turn ratinig \(0.0 ~ 5.0, 0.5unit\) |
| echo\_time | echo driving time |
| idle\_time | idle time \(days, hours, minutes, seconds, milliseconds\) |
| sum\_score | Driving score |
| sum\_dist | total distance \(Meter\) |
| sum\_time | total driving time \(Seconds\) |
| os\_dist | Speeding distance \(Meter\) |
| os\_time | Speeding time \(Seconds\) |
| os\_speed | Speed average \(km/h\) |
| lon | unused |
| lat | unused |

