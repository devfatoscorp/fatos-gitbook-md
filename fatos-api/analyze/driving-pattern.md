---
description: Analysis of your driving behaviors
---

# Driving Pattern

{% api-method method="get" host="https://maps.fatos.biz" path="/analysing/drivehistory/pattern" %}
{% api-method-summary %}
Driving Pattern
{% endapi-method-summary %}

{% api-method-description %}
Returns driving pattern statistics for distance and time charts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
  {
    "uuid": "355605080653378",
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

| Return Parameter | Description |
| :--- | :--- |
| uuid | UUID of the user |
| base\_time | Base date and time - Format varies by mode mode=0 : YYYY-MM \(2019-09\) mode=1 : YYYY-MM-DD HH24 \(2020-01-03 06\) mode=2 : YYYY-MM-DD \(2020-01-05\) mode=3 : YYYY-MM-DD WW \(2020-01 01\) =&gt; A few weeks per year\(01 ~ 56\) mode=4 : YYYY-MM \(2019-10\) |
| sum\_dist | Total distance \(Meter\) |
| sum\_time | Total driving time \(Seconds\) |
| night\_dist | Total night mileage \(Meter\) |
| night\_time | Total night driving time \(Seconds\) |

