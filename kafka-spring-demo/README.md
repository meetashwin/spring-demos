## Kafka Spring Demo

### Prerequisites
1. Zookeeper running on localhost:2181
2. Apache Kafka running on localhost:9092
3. Kafka topic named "first_topic" is created

### Run
```
mvn spring-boot:run
```

### How to use?

Send a message to topic using this API call
```
curl -X POST -F 'message=test' http://localhost:9000/kafka/publish
```


