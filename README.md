# kafka-indv

## Install Kafka first
- [kafka](http://apache.forsale.plus/kafka/2.6.0/kafka_2.13-2.6.0.tgz)

## Run Zookeeper Service (in C:\kafka folder)
- .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

## Run Kafka Service (in C:\kafka folder)
- .\bin\windows\kafka-server-start.bat .\config\server.properties

## Execute One-Time Commands - create, list topics (in kafka folder at C:)
- create .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic bearcat-messages
- list .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list

## Run Kafka Producer (type some words here)
- .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic bearcat-messages

## Run Kafka Consumer (will show what you type on last step)
- .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic bearcat-messages --from-beginning
