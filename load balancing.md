Load Balancing
======

##hardware load balancer
also called application delivery controller ([ADC](http://en.wikipedia.org/wiki/Application_delivery_controller)), but basically it's just a hardware load balancer

- F5: Big-IP
- Radware: Alteon NG
- Ctrix: Netscaler

## software load balancer
- [LVS](http://en.wikipedia.org/wiki/Linux_Virtual_Server)

### hardware vs software [ref] (http://serverfault.com/a/173229)
hardware load balancers are also full-fledged PC, implement a richer set of features.

## DMZ network
DMZ: a network exposing internal resources to external web. 

## proxy
-  **forward proxy** can be installed to provide outside internet access for internal resources
- **reverse proxy** can be placed into DMZ to allow outside to access internal resource.

solutions:

- squid
- haproxy


