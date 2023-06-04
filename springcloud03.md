## Notes On Spring Cloud




<br><br><br>

### Microservices Pattern ###
<br><br>

**Saga Transaction Pattern**

* How to do transactions that span services?
* Make each business transaction that spans across multiple services as a saga. A saga is a sequence of local transactions
* Saga Patter makes use of messages to publish in case we need to trigger the next local transaction
* What to do in case of failure 
* Saga will create compensating transaction to undo the records in the local databases
* Choreography - there are chain of local transactions triggered ; each local transaction publishes domain events that trigger other local transactions in another services
* Orchestration - here there is an orchestrator that tells the participants what local transactions to execute
 
 <br><br><br><br>
 
 **Reactive Microservices Pattern**
 <br><br>
*  Instead of writing blocking code with old web servers use netty reactive server and spring webflux

*  Return reactive types in spring boot controllers endpoints

*  Make microservices self-healing and resilient
 
 
