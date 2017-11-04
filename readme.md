# Vue Ping

## Description

A Pretty simple utility built with Vue.js to check if a domain is live or down.

There's no back-end where domains' details and their past status are stored.
But there's a JSON file name `data.json`, with which you can customize the sites this app is tracking.



## One Tiny Gotcha

This does work in `http://localhost`, since most private websites do not allow Cross Domain request, you would 
have to use a plugin like (Allow-Control-Allow-Origin) [https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi]
when working on `http://localhost`.



## data.json Configurations

There's not much you can configure, take a look in the code below.
``` json
[
  {
    "name": "Google IN",
    "url": "google.co.in",
    "port": 80
  },
  {
    "name": "Facebook",
    "url": "facebook.com"
  },
  {
    "name": "Some Random Site",
    "url": "somerandomsite.com",
    "port": 8080
  }
]
```