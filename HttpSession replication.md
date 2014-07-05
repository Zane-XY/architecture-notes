HttpSession Replication<sup>[ref](http://www.ibm.com/developerworks/library/j-jtp07294/)</sup>
======
- most servlet containers perform HttpSession replication by serializing objects stored in the HttpSession
- different containers have different strategies

## session persistence strategies 
- save to a same DB
- save to a same FS
- in-memory replication. serialized session object is copied to other nodes as failover backup . most time it is used with sticky session or called session affinity.
- shared external memory
- sticky session: load balancer will always route same session id to the same node (ASP.NET, Tomcat via mod_jk and Apache HTTPD)

