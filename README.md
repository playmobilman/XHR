# XHR:
XHR is a wrapper around Titanium's HTTPClient. It works perfectly with REST API endpoints and has a built in cache system that you can use for your requests. But it also can be use for any HTTP requests, you can even cache remote images.

## Usage:
In your app.js (or elsewhere), call:

```javascript
var XHR = require("/xhr");
var xhr = new XHR();
xhr.GET("http://freegeoip.net/json/", onSuccessCallback, onErrorCallback, options);
```

A quick explanation of the arguments in the `get()` mehtod of the previous code would look like this:

* **url**: (required) The URL where the API endpoint or content is located 
* **successCallback**: (required) Function to execute if the request succeeds 
* **errorCallback**: (optional) Function to execute if the request fails 
* **options**: (optional) Huge set of options for your request, please see the [examples.js](https://github.com/raulriera/XHR/blob/master/examples.js) file for more information.

For more information please check out the [examples.js](https://github.com/raulriera/XHR/blob/master/examples.js) file. Or browse around the [xhr.js](https://github.com/raulriera/XHR/blob/master/xhr.js) file. You can find in there support for GET, POST, PUT and DELETE (called destroy for reserved words problems)

## Helpers
Apart from the RESTful way of interacting with your API endpoints, this module also includes the following helper methods:

### clear(url)

* **url**: (required) The URL you want removed from the cache manager

Finds the cached document of the given url (if any) and removes it from the cache manager. This method is useful if you are not satisfied with the results you got at the time.

### clean()
Goes through all the cached documents and delete everything that has been expired (if their TTL timestamp is less than the current time)

This method returns the count of deleted documents

### purge()
Goes through all the documents and deletes everything

This method returns the count of deleted documents

## About:
Created by Raul Riera, [@raulriera](http://twitter.com/raulriera)  

Contributions by:

* Daniel Tamas, [@dan_tamas](https://twitter.com/dan_tamas) 
* Bob Sims, [@2wheelsburning](https://twitter.com/2wheelsburning) 
* Mark Ross [@rossman66](https://github.com/rossman66)
* Rene Pot, [@Wraldpyk](https://twitter.com/wraldpyk) 
