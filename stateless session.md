stateless session
======

## idea
client side managed session, store season data via cookie, app server doesn't manage session

### encoding 

- Demystifying Web Authentication<sup>[link](http://security.stackexchange.com/a/30714)</sup>
- Hardened Stateless Session Cookies<sup>[link](http://www.cl.cam.ac.uk/~sjm217/papers/protocols08cookies.pdf)</sup>
- Don't Roll Your Own Cryptography<sup>[ref](http://security.stackexchange.com/a/18198)</sup>

### pros
server side scalability, any sever can server any request without session syncrhonization

### cons
- cookie size limitation: 4K
- doesn't work if user disables browser cookie
- security issue: [session injection](http://www.playframework.com/security/vulnerability/20130806-SessionInjection) 


