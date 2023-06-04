## Notes On Spring Cloud 

```
package com.microservices.reactive.messaging;


import org.springframework.amqp.core.Queue;
import org.springframework.amqp.rabbit.annotation.RabbitListener;
import org.springframework.amqp.rabbit.core.RabbitMessagingTemplate;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.CommandLineRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.annotation.Bean;
import org.springframework.stereotype.Component;

@SpringBootApplication
public class Application implements CommandLineRunner {
	@Autowired
	Sender sender;

	
	public static void main(String[] args) {
		SpringApplication.run(Application.class, args);
	}
	
	@Override
    public void run(String... args) throws Exception {
    	sender.send("Hello Folks This is Reactive Microservice");
    }

}


@Component 
class Sender {
	@Autowired
	RabbitMessagingTemplate template;
	@Bean
	Queue queue() {
		return new Queue("NameQChanServiceAEvent", false);
	}
	public void send(String message){
		template.convertAndSend("NameQChanServiceAEvent", message);
	}
}


@Component
class Receiver {
    @RabbitListener(queues = "NameQChanServiceAEvent")
    public void processMessage(String content) {
       System.out.println(content);
    }
}

```

**Notes**

* <artifactId>spring-boot-starter-amqp</artifactId>

* <artifactId>spring-boot-starter-web</artifactId>

* No live connection, fire and forget 

<br><br>

