dynamic page caching
======

##concepts
**Edge server** is any server that resides on the "edge" between two networks <sup>[ref] (http://serverfault.com/a/67489)</sup>

```
                                     ----------> [internal app server]
 [browser] ----------> [edge server] ----------> [internal app server] 
                                     ----------> [internal app server]
```

**Edege Side Include** (ESI<sup>[ref](http://en.wikipedia.org/wiki/Edge_Side_Includes)</sup>) is a markup language for edge server side dynamic web content assembly

## fragment caching
application server serve page fragments, cache server re-assemble pages

## use cases<sup>[ref](http://esi-examples.akamai.com/)</sup> 
- dynamic page based on location, different state has different  promotion page
```xml 
<esi:include src="index$(GEO{'country_code'}|'US').html" alt="indexUS.html" ttl="2h" maxwait="5000"/>
```
- dynamic page based on cookie, logged in, shopping cart is full
```xml
<esi:when test="$(HTTP_COOKIE{'i'})"> ... 
```
- dynamic page based on time, set page TTL (time-to-live)
 
## architecture example
- php + nginx + memcached (nginx has native memcached support)
- varnish support ESI 

## caching reverse proxy vs CDN
- geographical vs local
- static vs dynamic
- resources interaction

## squid vs varnish<sup>[ref](http://qr.ae/Y4iXl)</sup>
- Squid: a forward proxy can be used as a reverse proxy, stable, more features
- Varnish: designed as a reverse proxy
