# Most useful curl flags

|Flag|Description|
|--|--|
|[-d (--data)](#add-post-data-to-request)|Data. Includes data in POST request|
|-b (--cookie)|Pass data in cookie header|
|-c (--cookie-jar)|Save cookie in file|
|--dns-ipv4-addr|Tell curl to bind to set address|
|--dns-ipv6-addr|Tell curl to bind to set address|
|-f (--form)|Pretend that user submit a form|
|-I (--head)|HEAD http method to get only headers|
|-H (--header)|Add header to request|
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

## Examples

### Add POST data to request

`curl -d a=1 -d b=2 -d @filename --data-raw email=hello@gmail.com --data-binary @filename1`