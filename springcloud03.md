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
 
 **Data Consistency**
 <br><br>
*  Eventual consistency states that our data will only be fully consistent due to problems of microservices and fine granularity of database separation
 
 
