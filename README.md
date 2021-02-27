# kafka-publisher
Apache Kafka Publisher Example using SpringBoot

Download kafka windows
Go to your windows directorey where you have downloaded the kafka for me i.e E:\Software\kafka_2.13-2.6.0
then run  following commands

# start zookeeper.start bat file like below

.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties


# start kafka server
.\bin\windows\kafka-server-start.bat .\config\server.properties


# Create Topic:
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1  --topic practice2

# Produce a message 
kafka-console-producer.bat --broker-list localhost:9092 --topic practice2

# Consume a message
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic practice2
