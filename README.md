# Most useful curl flags

|Flag|Description|
|--|--|
|[-d (--data)](#add-post-data-to-request)|Data. Includes data in POST request|
|[-G (--get)](#get-request)|Uses GET request instead of POST with --data option|
|[-X (--request)](#custom-request)|Users custom method to be requested|
|[-b (--cookie)](#set-cookie)|Pass data in cookie header|
|[-c (--cookie-jar)](#save-cookie)|Save cookie in file|
|-f (--form)|Pretend that user submit a form|
|[-I (--head)](#head-request)|HEAD http method to get only headers|
|[-H (--header)](#add-header)|Add header to request|
|--http1.1|Use HTTP1.1|
|--http2|Use HTTP2|
|-v (--verbose)|See all headers and responses|
|-i (--include)|Include response headers in output|
|-k (--insecure)|Ignore TLS errors|
|-4 (--ipv4)|Use IPv4 to connect|
|-6 (--ipv6)|Use IPv6 to connect|
|--interface |Use specific interface to connect|
|-L (--location)|Follow the redirect response|
|-o (--output)|Save output in file|
|-A (--user-agent)|Sets user agent to request|

[] and {} can be used in URL:

`curl https://example[1-100].com`

or with a step

`curl https://example[1-100:10].com`

or from set

`curl https://example.{a,b,c}.com`

## Examples

### Add POST data to request

`curl -d a=1 -d b=2 -d @filename --data-raw email=hello@gmail.com --data-binary @filename1 info.cern.ch`

### Get request

`curl -G -d hello=1 info.cern.ch`

### Custom request

`curl -X OPTIONS info.cern.ch`

### Set cookie

`curl -b hello=1 info.cern.ch`

### Save cookie

`curl -c cookie.txt info.cern.ch`

### HEAD request

`curl -I info.cern.ch`

### Add header

`curl -H "X-Content: SomeContent" info.cern.ch`