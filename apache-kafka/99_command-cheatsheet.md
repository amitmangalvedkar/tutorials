# Kafka Cheatsheet #

1. Running Kafka on Ubuntu (https://hevodata.com/blog/how-to-install-kafka-on-ubuntu/ )

2. Start kafka server  
```sudo /opt/kafka/bin/kafka-server-start.sh /opt/kafka/config/server.properties```

3. Delete a topic  
```/opt/kafka/bin/kafka-topics.sh --delete --zookeeper buildinginsights1.fyre.ibm.com:2181 --delete --topic test```

4. Create a topic   
```/opt/kafka/bin/kafka-topics.sh --create --zookeeper buildinginsights1.fyre.ibm.com:2181 --replication-factor 1 --partitions 1 --topic test```

5. List all topics with the command below   
```/opt/kafka/bin/kafka-topics.sh --list --zookeeper buildinginsights1.fyre.ibm.com:2181```

6. Publish messages on test topic   
```/opt/kafka/bin/kafka-console-producer.sh --broker-list buildinginsights1.fyre.ibm.com:9092 --topic test```

7. Create a subscriber on test topic and listen from the beginning of the topic.  
```/opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server buildinginsights1.fyre.ibm.com:9092 --topic test --from-beginning```

8. Enter some message in the producer
```Hello world!!!```
