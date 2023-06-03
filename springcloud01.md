## Notes On Spring Cloud ##




<br><br><br>

### Microservices Pattern ###
<br><br>

**Service Discovery Pattern**

Eureka - Used for Service Discovery Server & Service Discovery Client, written in Java

 **1.Per service Eureka saves Host and Port to the servicename**
 
 **2.There can be multiple Eureka Servers for HA**
 
 **3.Eureka Server polls each instance to check its availability**
 
 **4.Eureka Clients cache the config (reducing a roundtrip to the Eureka Server)** 
 
 <br><br><br><br>
 
 **Reactive Microservices Pattern**
 <br><br>
*  Instead of writing blocking code with old web servers use netty reactive server and spring webflux

*  Return reactive types in spring boot controllers endpoints

*  Make microservices self-healing and resilient
 
 
