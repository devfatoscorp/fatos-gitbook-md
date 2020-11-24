---
description: 'Search by POI such as airports, parks, mines, or gas station'
---

# POI

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/search/v1/total" %}
{% api-method-summary %}
POI Search
{% endapi-method-summary %}

{% api-method-description %}
Returns search results based on POI search queries and coordinate settings.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="kwd" type="string" required=true %}
Name search: search word  
Nearby search:  
category ID \(String to hex encoding\)  
  
i.e. {ABC Market} to {ec9db4eba788ed8ab8}
{% endapi-method-parameter %}

{% api-method-parameter name="stype" type="string" required=true %}
Search type  
Name search: 1  
Nearby search: 3
{% endapi-method-parameter %}

{% api-method-parameter name="cx" type="string" required=true %}
User's current location X coordinate \(wgs84\) \(Longitude\)
{% endapi-method-parameter %}

{% api-method-parameter name="cy" type="string" required=true %}
User's current location Y coordinate \(wgs84\) \(Latitude\)
{% endapi-method-parameter %}

{% api-method-parameter name="rad" type="string" required=true %}
Search radius \(Optional for name search\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
https://api.fatos.biz/search/v1/total?key=YOUR\_API\_KEY&stype=0&kwd=%EB%93%B1%EC%B4%8C%EC%97%AD&sort=0&cy=37.4827476&cx=126.89646959999999&sy=37.476471754823635&sx=126.96230592303937&pno=1&cpp=10&rad=1000
{% endapi-method-response-example-description %}

```javascript
{
   "err":null,
   "stype":0,
   "sort":0,
   "pgno":1,
   "cnt":5,
   "src_type":null,
   "data_type":1,
   "items":[
      {
         "id":null,
         "name":"등촌역 9호선",
         "name_en":null,
         "addr1":"서울특별시 양천구 공항대로 529",
         "addr2":"서울특별시 양천구 목동 666-94",
         "cate":"교통,운수>지하철,전철",
         "cate2":null,
         "phone":"",
         "posx":126.86557345606428,
         "posy":37.55076642169228,
         "entx":126.86557345606428,
         "enty":37.55076642169228,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":99,
         "flg":3,
         "dist":8036.588821067411
      },
      {
         "id":null,
         "name":"고양이똥",
         "name_en":null,
         "addr1":"서울특별시 강서구 공항대로59가길 13",
         "addr2":"서울특별시 강서구 등촌동 647-62",
         "cate":"음식점>브런치",
         "cate2":null,
         "phone":"",
         "posx":126.86467037619816,
         "posy":37.55210930478117,
         "entx":126.86467037619816,
         "enty":37.55210930478117,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":99,
         "flg":3,
         "dist":8204.10436532043
      },
      {
         "id":null,
         "name":"오봉집 등촌점",
         "name_en":null,
         "addr1":"서울특별시 양천구 목동중앙북로 7 신한상가 1층 101-2, 3호",
         "addr2":"서울특별시 양천구 목동 960",
         "cate":"한식>족발,보쌈",
         "cate2":null,
         "phone":"",
         "posx":126.86438087796013,
         "posy":37.548808734379264,
         "entx":126.86438087796013,
         "enty":37.548808734379264,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":99,
         "flg":3,
         "dist":7869.8820691089295
      },
      {
         "id":null,
         "name":"강서구보건소",
         "name_en":null,
         "addr1":"서울특별시 강서구 공항대로 561 강서보건소",
         "addr2":"서울특별시 강서구 염창동 275-12",
         "cate":"건강,의료>보건소",
         "cate2":null,
         "phone":"",
         "posx":126.8683623416128,
         "posy":37.54969388863684,
         "entx":126.8683623416128,
         "enty":37.54969388863684,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":99,
         "flg":3,
         "dist":7842.915750977192
      },
      {
         "id":null,
         "name":"통큰해물탕",
         "name_en":null,
         "addr1":"서울특별시 양천구 목동중앙북로5길 30",
         "addr2":"서울특별시 양천구 목동 608-1",
         "cate":"한식>매운탕,해물탕",
         "cate2":null,
         "phone":"",
         "posx":126.86612354925728,
         "posy":37.549564311671325,
         "entx":126.86612354925728,
         "enty":37.549564311671325,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":99,
         "flg":3,
         "dist":7894.442804525211
      }
   ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

