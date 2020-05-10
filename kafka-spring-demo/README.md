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
You should see the following messages in logs
-> Producing message -> test
-> Consumed message -> test

You can also use a console consumer to check the messages received on the topic
```
$kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first_topic
```
