---
description: Real-time monitoring and visualization
---

# Monitoring

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/mobilizer/users" %}
{% api-method-summary %}
Monitoring Data
{% endapi-method-summary %}

{% api-method-description %}
Gets control information necessary for real-time vehicle monitoring screen.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key. See the API Key Issuance page for information on using keys.
{% endapi-method-parameter %}

{% api-method-parameter name="uuid" type="string" required=true %}
UUID of the logged-in user.
{% endapi-method-parameter %}

{% api-method-parameter name="drive\_state" type="string" required=false %}
Driving Condition.  
0: All  
1: Live  
2: Stop  
3: Problem
{% endapi-method-parameter %}

{% api-method-parameter name="search" type="string" required=false %}
Search keyword \(uuid, license plate, username\)
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
    "device_type": "mobile",
    "license_plate": "SDY2933Q",
    "vehicle_model_id": "10000",
    "user_name": "yeon",
    "model": "iPad",
    "imei": "iOS 13.3",
    "phone_num": "",
    "create_date": "2019-11-17 15:07:26",
    "update_date": "2020-01-06 07:04:58",
    "lon": 126.98714147842026,
    "lat": 37.564932730501965,
    "addr": "",
    "total_dist": 1223747,
    "total_time": "74849",
    "today_dist": 0,
    "today_time": 0,
    "drive_state": 1,
    "latest_time": {
      "days": 9,
      "hours": 6,
      "minutes": 15,
      "seconds": 22,
      "milliseconds": 673.024
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

| Return Parameter | Description |
| :--- | :--- |
| uuid | UUID of the user |
| device\_type | Device type \( mobile, tracker \) |
| license\_plate | License plate |
| vehicle\_model\_id | Vehicle type \(truck : 10000, car : 10004, motorcycle : 10005, kickboard : 10006\) |
| user\_name | User name |
| model | Model name |
| imei | IMEI |
| phone\_num | Phone number |
| create\_date | Registration date |
| update\_date | Last update date |
| lon | User's last position X coordinate \(WGS84\) |
| lat | User's last position Y coordinate \(WGS84\) |
| addr | unused |
| total\_dist | Total distance \(Meter\) |
| total\_time | Total driving time \(Sec\) |
| today\_dist | The driving distance for the day \(Meter\) |
| today\_time | Total driving time on the day \(Sec\) |
| drive\_state | Driving condition \(0: all, 1: live, 2: stop, 3:problem\) |
| latest\_time | Final access idle time based on the current time \(days, hours, minutes, seconds, milliseconds\) |

