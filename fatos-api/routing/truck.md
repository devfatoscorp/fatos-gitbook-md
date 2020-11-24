---
description: Routing plan optimized for truck
---

# Route for truck

The Routing API will show you how to get where you’re going.   
With the Routing API, you can:

* Provide precise instructions to a destination using routing plans for various types of trucks
* To request directions, call four values: a start point, destination, and car type, and waypoint \(optional\).

{% hint style="info" %}
See the [**API Key Issuance page**](../../get-your-api-key.md) ****for information on using keys.
{% endhint %}

{% api-method method="get" host="https://api.fatos.biz" path="/fatos/api/route/truck" %}
{% api-method-summary %}
Routing API for truck
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="origin" type="string" required=true %}
Start point \(lat, lng\)
{% endapi-method-parameter %}

{% api-method-parameter name="destination" type="string" required=true %}
End point \(lat, lng\)
{% endapi-method-parameter %}

{% api-method-parameter name="key" type="string" required=true %}
Your API Key
{% endapi-method-parameter %}

{% api-method-parameter name="via" type="number" required=false %}
Waypoint \(lat, lng\), In the case of multiple waypoints, list them in order in the query string.
{% endapi-method-parameter %}

{% api-method-parameter name="cartype" type="integer" required=false %}
car type   
4. Heavy truck  
5. Very heavy truck  
7. Tank lorry  
8. Freight vehicle  
9. Construction vehicle
{% endapi-method-parameter %}

{% api-method-parameter name="rpoption" type="integer" required=false %}
Routing Plan Option  
Sum of each option value.  
1: Recommended 1  
2: Recommended 2  
4: Highway Priority  
8: General road Priority  
16: Shortest Distance  
32: Free road \(in the shortest time\)  
64: Exclude Car-only  
256: Free road \(in the shortest distance\)  
  
ex\) rpoption 3 =&gt; Recommended 1 + Recommended 2  
{% endapi-method-parameter %}

{% api-method-parameter name="angle" type="number" required=false %}
degrees \(0~359\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
https://api.fatos.biz/fatos/api/route?key=YOUR\_API\_KEY&origin=37.483294848898396,126.89654749206602&destination=37.51702306480502,127.0416190159097&angle=-1&rpoption=1&servicesvr=2&unixtime=1604626884&gmtoffset=32400&cartype=4&height=30&weight=30&length=30&uturn=4
{% endapi-method-response-example-description %}

```javascript
{
   "routes":[
      {
         "copyrights":"지도 데이터 ©2019 FATOS Co,. Ltd",
         "bounds":{
            "northeast":{
               "lat":37.519545462454886,
               "lng":127.04136930737667
            },
            "southwest":{
               "lat":37.48302259717505,
               "lng":126.89631925861033
            }
         },
         "legs":[
            {
               "distance":{
                  "text":"",
                  "value":17205
               },
               "duration":{
                  "text":"",
                  "value":1786
               },
               "start_address":"",
               "start_location":{
                  "lat":37.483155157904974,
                  "lng":126.89699827472333
               },
               "end_address":"",
               "end_location":{
                  "lat":37.51693525585199,
                  "lng":127.04136930737667
               },
               "steps":[
                  {
                     "attr":1839362,
                     "distance":{
                        "text":"",
                        "value":28
                     },
                     "duration":{
                        "text":"",
                        "value":16
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.483155157904974,
                        "lng":126.89699827472333
                     },
                     "end_location":{
                        "lat":37.48302259717505,
                        "lng":126.89727579394929
                     },
                     "maneuver":"2",
                     "htmlInstructions":"|||||||좌회전",
                     "laneguide":"",
                     "polyline":{
                        "points":"ehxnfAkud`qFhGkP",
                        "mbr":{
                           "minx":126.89699827472333,
                           "miny":37.48302259717505,
                           "maxx":126.89727579394929,
                           "maxy":37.483155157904974
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":1839365,
                     "distance":{
                        "text":"",
                        "value":95
                     },
                     "duration":{
                        "text":"",
                        "value":56
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.48302259717505,
                        "lng":126.89727579394929
                     },
                     "end_location":{
                        "lat":37.48375788007269,
                        "lng":126.89783273974984
                     },
                     "maneuver":"5",
                     "htmlInstructions":"|||||디지털로32길||완만한 우회전",
                     "laneguide":"",
                     "polyline":{
                        "points":"}_xnfAwfe`qF}l@ya@",
                        "mbr":{
                           "minx":126.89727579394929,
                           "miny":37.48302259717505,
                           "maxx":126.89783273974984,
                           "maxy":37.48375788007269
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":1586434,
                     "distance":{
                        "text":"",
                        "value":62
                     },
                     "duration":{
                        "text":"",
                        "value":11
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.48375788007269,
                        "lng":126.89783273974984
                     },
                     "end_location":{
                        "lat":37.48369779859078,
                        "lng":126.89855276385839
                     },
                     "maneuver":"2",
                     "htmlInstructions":"|디지털로32길||||디지털로34길||좌회전",
                     "laneguide":"1/1/0/2,3/0/3/1,0",
                     "polyline":{
                        "points":"{mynfAqif`qF|@md@JgAl@iD",
                        "mbr":{
                           "minx":126.89783273974984,
                           "miny":37.48369779859078,
                           "maxx":126.89855276385839,
                           "maxy":37.48375788007269
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":1585923,
                     "distance":{
                        "text":"",
                        "value":339
                     },
                     "duration":{
                        "text":"",
                        "value":54
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.48369779859078,
                        "lng":126.89855276385839
                     },
                     "end_location":{
                        "lat":37.4857920673887,
                        "lng":126.89631925861033
                     },
                     "maneuver":"3",
                     "htmlInstructions":"|디지털로34길||||디지털로||우회전",
                     "laneguide":"0/1/0/1/0/2",
                     "polyline":{
                        "points":"cjynfAqvg`qFgI}FkC}@wCSyGDsHhAsH|A??kGfCwDbC}EzHgBhE??}Tbl@??uF|N??yAnD??wYnt@",
                        "mbr":{
                           "minx":126.89631925861033,
                           "miny":37.48369779859078,
                           "maxx":126.8987196568637,
                           "maxy":37.4857920673887
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":1594372,
                     "distance":{
                        "text":"",
                        "value":1601
                     },
                     "duration":{
                        "text":"",
                        "value":198
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.4857920673887,
                        "lng":126.89631925861033
                     },
                     "end_location":{
                        "lat":37.49686136517451,
                        "lng":126.90827642718432
                     },
                     "maneuver":"4",
                     "htmlInstructions":"선프라자|디지털로||||신길로||완만한 좌회전",
                     "laneguide":"0/0/1,2/0/0/2",
                     "polyline":{
                        "points":"_m}nfA}jc`qFwt@_i@??kMuI??_HsE??wN{K??wBaC??wO}P??cBaB??e@o@??s\\}c@??_AkA??sHaJ??gFiG??eSyU??_Xc[??cI{I??mAyA??gHcI??eByB??aFgG??cC}C??uG{H??qH}I??oHqI??e^uc@??kQcS??w]u`@??gKiL??aToU??sN{O??gF}F??{QgT??aCwC??yBuC??k_@mc@??yEwF??}RwS??wg@kl@??wA_B??qKwL??aFwF??iN}O??y[__@??eZ}]??iJ{L??cMiO??aLaN??wEwF??iEiF??eGaI",
                        "mbr":{
                           "minx":126.89631925861033,
                           "miny":37.4857920673887,
                           "maxx":126.90827642718432,
                           "maxy":37.49686136517451
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":271078413,
                     "distance":{
                        "text":"",
                        "value":1691
                     },
                     "duration":{
                        "text":"",
                        "value":184
                     },
                     "traffic":0,
                     "start_location":{
...
...
...
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.50784292492327,
                        "lng":126.99956213271184
                     },
                     "end_location":{
                        "lat":37.505004790158836,
                        "lng":127.00092016493784
                     },
                     "maneuver":"2",
                     "htmlInstructions":"고속터미널|반포대로||||신반포로||좌회전",
                     "laneguide":"1/1,2/0/3,4/0/5/2,0",
                     "polyline":{
                        "points":"eohpfAs_mfqFrfCs~@??nKiE??|LcF??~EiBjGoC",
                        "mbr":{
                           "minx":126.99956213271184,
                           "miny":37.505004790158836,
                           "maxx":127.00092016493784,
                           "maxy":37.50784292492327
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":1598979,
                     "distance":{
                        "text":"",
                        "value":3777
                     },
                     "duration":{
                        "text":"",
                        "value":463
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.505004790158836,
                        "lng":127.00092016493784
                     },
                     "end_location":{
                        "lat":37.51720514568342,
                        "lng":127.04127584729372
                     },
                     "maneuver":"3",
                     "htmlInstructions":"강남구청역|학동로||||선릉로||우회전",
                     "laneguide":"1/1/0/2,3,4/0/4/1,0",
                     "polyline":{
                        "points":"y}bpfAotofqFh@_R??sEeU??kQg{@??aW{iA??qGmY??gAqFsHg^??oK_h@gB}I??qe@}aC??}Mqs@??_FcW??{AsI??gFwU??sc@kbC??oCoM??}UcnA??ee@wxB??}Lql@??yJoe@??c@yB??{Ly[??m@oC??kUycA??mFgZ??wCkO??qFiY??gBaI??oGe[??uB{K??oEuU??mNys@??iDiO??oKii@??aJaf@??qIo`@??aAsG??gKkc@??sIka@??kJwc@??yEqU??cGi[??wPew@??iMqp@??{C{N??mCyK??sHe]??eNuo@??mH__@??sNor@??wO}t@??_Z}xA??oLai@??iMsk@??uNgs@??{CuN??_Leh@??uA_H??iDwP??wIyb@??iKuf@??qFkW??cNqq@??mNkp@??mK_g@??gN_t@",
                        "mbr":{
                           "minx":127.00092016493784,
                           "miny":37.5049838093239,
                           "maxx":127.04127584729372,
                           "maxy":37.51720514568342
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  },
                  {
                     "attr":1598514,
                     "distance":{
                        "text":"",
                        "value":31
                     },
                     "duration":{
                        "text":"",
                        "value":1
                     },
                     "traffic":0,
                     "start_location":{
                        "lat":37.51720514568342,
                        "lng":127.04127584729372
                     },
                     "end_location":{
                        "lat":37.51693525585199,
                        "lng":127.04136930737667
                     },
                     "maneuver":"50",
                     "htmlInstructions":"|선릉로|선릉역|||||목적지가 있습니다 ",
                     "laneguide":"0/0/0/1,2/0/2",
                     "polyline":{
                        "points":"ixzpfAwn~hqFzOyD",
                        "mbr":{
                           "minx":127.04127584729372,
                           "miny":37.51693525585199,
                           "maxx":127.04136930737667,
                           "maxy":37.51720514568342
                        }
                     },
                     "travelMode":"DRIVING",
                     "roadObject":"",
                     "complexIntersection":"",
                     "serviceArea":"",
                     "tollgate":""
                  }
               ],
               "trafficSpeedEntryList":[
                  
               ],
               "viaWaypoints":[
                  
               ]
            }
         ],
         "overviewPolyline":{
            "points":"ehxnfAkud`qFhGkP??}l@ya@??|@md@JgAl@iD??gI}FkC}@wCSyGDsHhAsH|A??kGfCwDbC}EzHgBhE??}Tbl@??uF|N??yAnD??wYnt@??wt@_i@??kMuI??_HsE??wN{K??wBaC??wO}P??cBaB??e@o@??s\\}c@??_AkA??sHaJ??gFiG??eSyU??_Xc[??cI{I??mAyA??gHcI??eByB??aFgG??cC}C??uG{H??qH}I??oHqI??e^uc@??kQcS??w]u`@??gKiL??aToU??sN{O??gF}F??{QgT??aCwC??yBuC??k_@mc@??yEwF??}RwS??wg@kl@??wA_B??qKwL??aFwF??iN}O??y[__@??eZ}]??iJ{L??cMiO??aLaN??wEwF??iEiF??eGaI??s^bC??{WjB??sRLuMeB??w~@{R??m^uJiLmF}CqA??oEoBmH}G??gC_C??c_@y\\kQkMyj@iV??oCeAaQeDaMq@mNp@??cMj@??wMbBqWnCmJx@??cGRmE_@qIaCwHaD??}TcJ??wXaLyE_B??eGiC??aZmI??wKeB??}EM??co@jA??_^`A??qZz@??aW^??cQT??gQn@??uKx@eH|@oXhG??cPhD??aFdA??kGzA??_AT??cQfCgO|C??mLrC??}`@bK??yO|D??_@FaBDaCFwB?eDO??oCUmDm@??wCm@cHqDqEuCiFwC??wMwH??yz@yl@??kd@i[??gv@qh@??}BsA??cBaA??iGqCgCi@oCUgD?{aCtKuHR??wAC??u@AsACgDQ??eEM??qMga@??a@sA??cAcD??eKkY??eCgHeCsGoAgC}@qAya@cg@??eAaKEeETcEd@sCd@cA??hF_EjKoItD{CpGkG|IqJ`M_QtMiTfPea@fI_WxDwW??tBiH|r@k`C??nL}c@??jGuW??pTu~@~XcjAba@gyA??tFiYvHsa@hIoh@xD_\\jCgZ|As\\nAa_@t@_a@H}]C{Sw@k_@??a@sUsM}qDaIuzA??RmeAmGov@??qKylAgHgx@??kCmWaGul@??wCcZ??uLevA??iIqTug@k}@yGoNsHkSuEaReEw[yBkR??cBkO??Pqr@??p@mh@l@uu@??rBgLxA}GdAyEzEePnCqIbImTrDuJfIyQzIiQjFyLxGeQvF_PjGqRnEuOvCwLrByI~Is`@??lCeVdEmWdFaZ??pFs\\bE{UxHid@tEmWxFyYnG_[fH{[pHg[~L{e@vNqh@dLs_@jN_c@hHaT~Mc_@fOs`@jPm`@dP__@h^iw@vc@y`AhPc^vRmb@bRsa@bKoU~KiXrLyZlMq^jLi]rNge@`Lua@rHuYxLch@pHk\\rH_[lIe[jJa[rKeZrLkZlMsXxNoY~U{b@tNmWzMaXlLaX??xJ{YnIkZjI__@??hDkV|AuQ~Aca@v@{\\h@}b@??p@ceB??h@uhACca@Sw_@]_V}@}WeAiS}AkTeBeUgByQqB_RaDaXaFoa@gFoa@sK}|@kCsWoFmf@iFkb@cEm]cGgc@eOst@_Iu]??aB_GaGqQ}o@goB??yD_Ue{@}lCy\\wgAoEaN}Nyb@oAmDsGcR??]iI|@aHzAmG`AgDzB}FbB_C??`xA{g@??rfCs~@??nKiE??|LcF??~EiBjGoC??h@_R??sEeU??kQg{@??aW{iA??qGmY??gAqFsHg^??oK_h@gB}I??qe@}aC??}Mqs@??_FcW??{AsI??gFwU??sc@kbC??oCoM??}UcnA??ee@wxB??}Lql@??yJoe@??c@yB??{Ly[??m@oC??kUycA??mFgZ??wCkO??qFiY??gBaI??oGe[??uB{K??oEuU??mNys@??iDiO??oKii@??aJaf@??qIo`@??aAsG??gKkc@??sIka@??kJwc@??yEqU??cGi[??wPew@??iMqp@??{C{N??mCyK??sHe]??eNuo@??mH__@??sNor@??wO}t@??_Z}xA??oLai@??iMsk@??uNgs@??{CuN??_Leh@??uA_H??iDwP??wIyb@??iKuf@??qFkW??cNqq@??mNkp@??mK_g@??gN_t@??zOyD",
            "mbr":{
               "minx":0,
               "miny":0,
               "maxx":0,
               "maxy":0
            }
         },
         "summary":"신길로|올림픽대로|신반포로",
         "warnings":"",
         "waypointOrders":[
            
         ],
         "rpoption":1
      }
   ],
   "status":200,
   "statusMsg":""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="warning" %}
**Display of Directions Results**

After you receive the requested results, you must decode the result into a geometry code. Call the Fatos.polyLine\(\) function as the decoded result and display the result on the map.
{% endhint %}

