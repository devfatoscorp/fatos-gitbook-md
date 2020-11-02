---
description: Driving distance and time for given dates
---

# Driving Mileage Statistic

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://maps.fatos.biz" path="/analysing/drivepattern/mileage" %}
{% api-method-summary %}
Returns driving pattern statistics for distance and time on the Analyze page
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mode" type="string" required=false %}
Period categorization  
0: By months  
1: By hours  
2: By days  
3: By weeks  
4: By months
{% endapi-method-parameter %}

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
    "uuid": "355605080653378",
    "base_time": "2019-12",
    "sum_dist": 13221742,
    "sum_time": 4208,
    "night_dist": 0,
    "night_time": 456
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



