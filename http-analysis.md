# Module 1: HTTP Analysis

## Request 1: json Document
* **Request Method:** GET
* **URL:**https://sdk.nsureapi.com/core-config/config.json
* **Status Code:** 200 OK
* **Response Headers:**
  * content-typeapplication/json
  * x-cache Hit from cloudfront
11.99ms


## Request 2: HTML Doc
* **Request Method:** GET
* **URL:** https://sdk.nsureapi.com/sdkIframe.html
* **Status Code:** 200 OK 
* **Response Headers:**
  * content-typetext/html
  * Date Sun, 27 Sep 2026 14:58:00 GMT

16.93ms


## Request 3: monitor
* **Request Method:**POST
* **URL:** https://analytics.tiktok.com/api/v2/monitor
* **Status Code:** 200 OK
* **Response Headers:**
  * Server nginx
  * access-control-allow-methods GET,POST,PUT,PATCH,DELETE,HEAD,OPTIONS,UPDATE

duration 185.03ms

## Technical Analysis
The slowest request was the monitor request, i would assume that this request was the longest due to the fact that 
this monitor is utilized to track the effectiveness of tiktok advertizing campagins. Which means this has to filter
alot of data aswell as do numerious otherthings aswell. One header that sucsessfuly commanded my browser to change
its behavior would be the x-cache Hit from cloudfront. This header sucsessfuly had loaded the website from an 
amazon cloud server. One thing that supprised me was the fact that the monitor request allowes so many different 
types of requests.