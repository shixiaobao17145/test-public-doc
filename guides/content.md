<seotitle>REST API Name content compression and encoding, 50–60 chars</seotitle>

# Content Compression and Encoding

_> If the API results or headers must have particular indicators for compression or encoding, let the user know in this section._

_> Include any [HTTP header](https://apistyleguide.cisco.com/#!rest-style/using-http-headers\) details like supported content types, UTF-8 encoding, response compression, default settings, and headers required for specific features._

_> Example based on SD-WAN. Expand this section to document the various encodings and other customizations your API supports:_

vManage API by default uses UTF-8 character set encoding.

Gzip compression is not set by default. To enable gzip compression, provide the following HTTP request header:

```
Accept-Encoding: gzip
```

The API response contains the following HTTP response header to indicate that the code must first decompress using Gzip before processing the response payload:

```
Content-Encoding: gzip
```
