

## Notes On Spring Cloud##




<br><br><br>

### Microservices Pattern ###
<br><br>

**Edge Server Pattern**

In microservices world it is advisable to secure some services from the public access thru the internet therefore in spring cloud there is 
a component hte spring cloud gateway. This component acts as the reverse proxy , all incoming request to our microservices or API will first
pass thru this.
 
 **1. Implementing this may require you to expose the endpoints and still protect these with JWT**
 
 **2. You might hide specific services that are required only by internal microservices**
 
 **3. Spring cloud gateway may be integrated with discovery service**
 <br><br>
 <br><br>
  
  
  
  
  
 **Distributed Tracing Pattern**
 <br><br>
*  How can we trace the transactions of cooperating microservices

*  Add correlation ID for logging of the microservices transaction

*  This requires that every request has timestamp tracing ID  and useful meta data for a central logging service to collect





 
