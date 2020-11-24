---
description: Find a location by an address
---

# Address

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/search/v1/addr" %}
{% api-method-summary %}
Address
{% endapi-method-summary %}

{% api-method-description %}
Returns search results based on address search queries and coordinate settings
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
Your API Key.
{% endapi-method-parameter %}

{% api-method-parameter name="kwd" type="string" required=true %}
Search word \(string to hex encoding\)  
{Ogeumno182} to {ec98a4eab888eba19c313832}
{% endapi-method-parameter %}

{% api-method-parameter name="stype" type="string" required=true %}
Search type: 2 \(for address search\)
{% endapi-method-parameter %}

{% api-method-parameter name="cx" type="string" required=true %}
User's current location X coordinate \(wgs84\) \(Longitude\)
{% endapi-method-parameter %}

{% api-method-parameter name="cy" type="string" required=true %}
User's current location Y coordinate \(wgs84\) \(Latitude\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
https://api.fatos.biz/search/v1/addr?key=YOUR\_API\_KEY&stype=0&kwd=cafe&cy=13.75359860777786&cx=100.4985572291215&sy=13.75359860777786&sx=100.4985572291215&pno=1&cpp=10&rad=10000&lang=en
{% endapi-method-response-example-description %}

```javascript
{
   "err":null,
   "stype":0,
   "sort":0,
   "pgno":1,
   "cnt":10,
   "src_type":null,
   "data_type":1,
   "items":[
      {
         "id":"ChIJGeftrN2e4jARJNTfjce9KBQ",
         "name":"Café Tartine",
         "name_en":null,
         "addr1":"65 2 Witthayu Rd, Lumphini, Pathum Wan District, Bangkok 10330, Thailand",
         "addr2":"",
         "cate":"meal_takeaway",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5496198,
         "posy":13.7419341,
         "entx":100.5496198,
         "enty":13.7419341,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":5670.87887856292
      },
      {
         "id":"ChIJP7GglFKf4jARw3wkrY5GKT8",
         "name":"CAFE' DE BLUE",
         "name_en":null,
         "addr1":"270 ซอย จันทน์ 18/7 Thung Wat Don, Sathon, Bangkok 10120, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5267889,
         "posy":13.7111353,
         "entx":100.5267889,
         "enty":13.7111353,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":5602.736733637275
      },
      {
         "id":"ChIJT_p7Pbie4jARooqGAPe4-2Y",
         "name":"Chibi Chibi",
         "name_en":null,
         "addr1":"Rang Nam Alley, Thanon Phaya Thai, Ratchathewi, Bangkok 10400, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.541717,
         "posy":13.75849,
         "entx":100.541717,
         "enty":13.75849,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":4698.556870648395
      },
      {
         "id":"ChIJRZ77g86f4jARJjlg0RKKgss",
         "name":"Phak Cafe & Crafts",
         "name_en":null,
         "addr1":"1 Sukhumvit 51 Alley, Khlong Tan Nuea, Watthana, Bangkok 10110, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5765161,
         "posy":13.726134,
         "entx":100.5765161,
         "enty":13.726134,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":8961.895098449526
      },
      {
         "id":"ChIJYY4hWhCZ4jARs23g1bHzSQM",
         "name":"NO.14 CAFE",
         "name_en":null,
         "addr1":"14 Ratchabophit Rd, แขวง วัดราชบพิธ Phra Nakhon, Bangkok 10200, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.498308,
         "posy":13.7495121,
         "entx":100.498308,
         "enty":13.7495121,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":452.88777198751006
      },
      {
         "id":"ChIJJ3iMaMWY4jAREYZ5qjNM0MI",
         "name":"Cafe Mozu",
         "name_en":null,
         "addr1":"1055 Si Lom, Silom, Bang Rak, Bangkok 10500, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5172142,
         "posy":13.7212052,
         "entx":100.5172142,
         "enty":13.7212052,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":4112.629066388228
      },
      {
         "id":"ChIJA0ixSIue4jARArXdko69EFY",
         "name":"PRESSED CAFE",
         "name_en":null,
         "addr1":"61/120 Rama IX Soi 7, Khwaeng Huai Khwang, Huai Khwang, Bangkok 10310, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5702246,
         "posy":13.7564121,
         "entx":100.5702246,
         "enty":13.7564121,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":7756.430556933887
      },
      {
         "id":"ChIJNcOJUpWd4jARCJwNkAg-jMU",
         "name":"Woolloomooloo Cafe & Bar",
         "name_en":null,
         "addr1":"145 Soi Vibhavadi Rangsit 16, Khwaeng Din Daeng, Din Daeng, Bangkok 10400, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5730002,
         "posy":13.7978446,
         "entx":100.5730002,
         "enty":13.7978446,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":9421.110370850358
      },
      {
         "id":"ChIJEYK-S1Ke4jARoB8EQyagLWc",
         "name":"Tiny Cup Cafe",
         "name_en":null,
         "addr1":"Thonglor Rd, Khlong Tan Nuea, Watthana, Bangkok 10110, Thailand",
         "addr2":"",
         "cate":"restaurant",
         "cate2":"establishment",
         "phone":null,
         "posx":100.5836806,
         "posy":13.7375186,
         "entx":100.5836806,
         "enty":13.7375186,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":9376.034369843605
      },
      {
         "id":"ChIJjQL_0hOZ4jARDqTTTH2DjFw",
         "name":"3rd Cafe",
         "name_en":null,
         "addr1":"20 Thanon Mahannop, Sao Chingcha, Phra Nakhon, Bangkok 10200, Thailand",
         "addr2":"",
         "cate":"cafe",
         "cate2":"establishment",
         "phone":null,
         "posx":100.4987724,
         "posy":13.7536741,
         "entx":100.4987724,
         "enty":13.7536741,
         "hassub":0,
         "pid":null,
         "entries":null,
         "props":null,
         "geom":null,
         "wgpt":null,
         "src":98,
         "flg":3,
         "dist":24.72196689199433
      }
   ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

