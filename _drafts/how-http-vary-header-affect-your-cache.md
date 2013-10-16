The Vary header is a HTTP header whereby a HTTP server can indicate to itermediate caches that the contents of the URI varies based on specified aspects of the client request.

The Vary header is sent by the web server to indicate what makes a HTTP object Vary. This makes a lot of sense with headers like Accept-Encoding. When a server issues a "Vary: Accept-Encoding" it tells Varnish that its needs to cache a separate version for every different Accept-Encoding that is coming from the clients. So, if a clients only accepts gzip encoding Varnish won't serve the version of the page encoded with the deflate encoding.

Vary: Accept-Encoding
Vary: Accept-Encoding,User-Agent
Vary: X-Some-Custom-Header,Host
Vary: *
