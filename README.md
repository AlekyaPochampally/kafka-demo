# kafka-demo

## My notes on kafka commands
- Run Zookeeper Service 
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

- Run Kafka Service
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

- create, list, delete topics 
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic university_and_covid19-messages

.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```

 - Run Kafka Producer ( > will be prompted for writing messages)
```
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic univeristy_and_covid19-messages
```

 - Run Kafka Consumer (to show messages from the beginning)
 ```
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic univeristy_and_covid19-messages --from-beginning
```
