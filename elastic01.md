## Notes On Spring Cloud


<br>

**What Is Elasticsearch**

*  Uses Apache Lucene
*  Efficient search - acts as a near real-time search platform
<br><br>

**Spring Data Elasticsearch**





**Spring POM XML**

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <parent>
       ...
    </parent>
       ...
    <properties>
        <java.version>17</java.version>
        <springdoc-openapi-ui.version>1.5.13</springdoc-openapi-ui.version>
    </properties>
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-elasticsearch</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-devtools</artifactId>
            <scope>runtime</scope>
            <optional>true</optional>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
        </dependency>
 
        
    </dependencies>
   ... 
</project>
```



**Important App Properties**


```

# ELASTICSEARCH
elasticsearch.host=127.0.0.1
elasticsearch.port=9200


```




<br><br>

```
 

import lombok.Getter;
import lombok.Setter;
import org.springframework.data.annotation.Id;
import org.springframework.data.elasticsearch.annotations.Document;
import org.springframework.data.elasticsearch.annotations.Field;
import org.springframework.data.elasticsearch.annotations.FieldType;

@Document(indexName = "car")
@Getter @Setter
public class Cars {
    @Id
    private String id;

    @Field(type = FieldType.Text, name = "name")
    private String carname;
    
     @Field(type = FieldType.Text, name = "model")
    private String model;
}
```


**Repository**

```
...
 
import org.springframework.data.elasticsearch.repository.ElasticsearchRepository;
import org.springframework.stereotype.Repository; 
@Repository
public interface CarRepository extends ElasticsearchRepository<Cars, String> {
}
```


**Controller Endpoints**

``` 
import org.elasticsearch.ResourceNotFoundException;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.*;

@RestController
@RequestMapping("api/cars") 
public class CrudController {

    @Autowired
    private CarRepository carsRepoClass;

    @PostMapping(value = "/", consumes = "application/json")
    public Cars create(@RequestBody Cars car) {
        return carsRepoClass.save(car);
    }

    @GetMapping(value = "/{id}", produces = "application/json")
    public Cars retrieve(@PathVariable String id) {
        return carsRepoClass.findById(id).orElseThrow(() -> new ResourceNotFoundException("ID: " + id));
    }
    ...

```


**Our Application Class**

``` 
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.annotation.ComponentScan;
import org.springframework.data.elasticsearch.repository.config.EnableElasticsearchRepositories;

@SpringBootApplication
@EnableElasticsearchRepositories(basePackages = "com.elastic.cars.repository") 
public class ApplicationCarSearchEngine {
    public static void main(String[] args) {
        SpringApplication.run(ApplicationCarSearchEngine.class, args);
    }
}
```
