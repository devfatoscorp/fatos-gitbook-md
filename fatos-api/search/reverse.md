---
description: Convert geographic coordinates into addresses
---

# Geocoding

Geocoding uses latitude and longitude information to provide an address. An optional description of the zoom level provides information suitable for the OpenLayers room level.

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/search/v1/geocoding" %}
{% api-method-summary %}
Reverse Geocoding
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="cy" type="string" required=true %}
Latitude of the search target
{% endapi-method-parameter %}

{% api-method-parameter name="cx" type="string" required=true %}
Longitude of the search target
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
https://api.fatos.biz/search/v1/geocoding?key=YOUR\_API\_KEY&cy=37.481154270115184&cx=126.95335681995971&lang=ko
{% endapi-method-response-example-description %}

```javascript
{
   "err":null,
   "stype":4,
   "sort":2,
   "pgno":1,
   "cnt":7,
   "src_type":null,
   "data_type":0,
   "items":[
      {
         "id":"1162010100109790001",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구 봉천동 979-1",
         "addr2":"",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953082616,37.48190784],[126.95330847,37.481852713],[126.952992684,37.48145277],[126.953019523,37.481370195],[126.953970253,37.481000056],[126.953972299,37.480983298],[126.953966091,37.480968249],[126.953971821,37.48085013],[126.953936844,37.480740554],[126.953947977,37.480658658],[126.953946971,37.480640637],[126.953956492,37.480604601],[126.95294559,37.48100024],[126.952841556,37.480961606],[126.952722832,37.480198948],[126.95272197,37.481489002],[126.952762336,37.481501254],[126.953082616,37.48190784]]]}",
         "posx":126.9532312,
         "posy":37.481133,
         "entx":126.9532312,
         "enty":37.481133,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":11,
         "wgpt":null,
         "src":9,
         "flg":1
      },
      {
         "id":"1162010100108580007",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구 봉천동 858-7",
         "addr2":"",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953284751,37.481491366],[126.953577002,37.481335462],[126.95346229,37.481199308],[126.953280623,37.481270556],[126.953255657,37.481291232],[126.953209704,37.481401144],[126.953284751,37.481491366]]]}",
         "posx":126.9533785,
         "posy":37.4813406,
         "entx":126.9533785,
         "enty":37.4813406,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":21,
         "wgpt":null,
         "src":9,
         "flg":1
      },
      {
         "id":"1162010100200000318270000",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구  남부순환로 1827",
         "addr2":"서울특별시 관악구 봉천동 858-7",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953318581,37.481325593],[126.953276804,37.481414235],[126.953309794,37.481452541],[126.953561773,37.481327404],[126.953491279,37.481239708],[126.953318581,37.481325593]]]}",
         "posx":126.9534118,
         "posy":37.4813443,
         "entx":126.9533892,
         "enty":37.4813376,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":22,
         "wgpt":null,
         "src":9,
         "flg":1
      },
      {
         "id":"1162010100200000318310000",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구  남부순환로 1831",
         "addr2":"서울특별시 관악구 봉천동 852-5",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953549992,37.481185312],[126.953613701,37.481275257],[126.953792607,37.481205232],[126.953737606,37.481111596],[126.953549992,37.481185312]]]}",
         "posx":126.9536733,
         "posy":37.481194,
         "entx":126.9537251,
         "enty":37.4811351,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":28,
         "wgpt":null,
         "src":9,
         "flg":1
      },
      {
         "id":"1162010100108520005",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구 봉천동 852-5",
         "addr2":"",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953630459,37.481298227],[126.953820028,37.481228668],[126.953733931,37.481093212],[126.953528854,37.481173775],[126.953630459,37.481298227]]]}",
         "posx":126.9536781,
         "posy":37.4811973,
         "entx":126.9536781,
         "enty":37.4811973,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":29,
         "wgpt":null,
         "src":9,
         "flg":1
      },
      {
         "id":"1162010100108580014",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구 봉천동 858-14",
         "addr2":"",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953117782,37.481612084],[126.953255657,37.481291232],[126.953280623,37.481270556],[126.953019523,37.481370195],[126.952992684,37.48145277],[126.953117782,37.481612084]]]}",
         "posx":126.9531177,
         "posy":37.48143,
         "entx":126.9531177,
         "enty":37.48143,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":37,
         "wgpt":null,
         "src":9,
         "flg":1
      },
      {
         "id":"1162010100109770000",
         "name":null,
         "name_en":null,
         "addr1":"서울특별시 관악구 봉천동 977",
         "addr2":"",
         "cate":null,
         "cate2":null,
         "geom":"{\"type\":\"Polygon\",\"coordinates\":[[[126.953272389,37.481806143],[126.95330847,37.481852713],[126.953865165,37.481673637],[126.954072514,37.481612058],[126.954054217,37.481582678],[126.954032519,37.481566992],[126.953983875,37.481575775],[126.953915368,37.481598451],[126.953861458,37.481584563],[126.953528854,37.481173775],[126.95346229,37.481199308],[126.953797894,37.481603511],[126.953783793,37.481641266],[126.953272389,37.481806143]]]}",
         "posx":126.9536755,
         "posy":37.4815705,
         "entx":126.9536755,
         "enty":37.4815705,
         "hassub":0,
         "phone":null,
         "pid":null,
         "entries":null,
         "props":null,
         "dist":54,
         "wgpt":null,
         "src":9,
         "flg":1
      }
   ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

