# Vue Ping

## Description
![Screen shot of Vue Ping](https://github.com/skadimoolam/ping/raw/master/screenshot.png "Screenshot of Vue Ping")


## Description

A Pretty simple utility built with Vue.js to check if a domain is live or down.

Demo at https://skadimoolam.github.io/ping/

There's no back-end where domains' details and their past status are stored.
But there's a JSON file name `data.json`, with which you can customize the sites this app is tracking.



## How does it work

Vue sends a `fetch` request to the specified url, if it returns `status: 200` then it's most likely alright.
To get around `cros` issue, this just sends an opaque request, for which most server respond without the actual
content of their site, but the usual headers are present.


## Usage

Just clone this repo anywhere the browser can reach and update the `data.json` with your sites.

This also has included support for Google Analytics, just switch the Property Id from Google, or you 
remove it completely.


## data.json Configurations

There's not much you can configure, take a look in the code below. Add or remove any site, should work as expected
if not just make an issue here in Github.
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

## License
MIT License

Copyright (c) 2017 Adi <skadimoolam@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.