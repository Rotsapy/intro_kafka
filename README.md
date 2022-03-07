# intro_kafka

Producers are those client applications that publish (write) events to Kafka

Consumers are those that subscribe to (read and process) these events

Setting up default values in this two files :
config/zookeeper.properties and config/server.properties


1 - start Zookeeper :
zookeeper-server-start config/zookeeper.properties

2 - start kafka server :
kafka-server-start config/server.properties

3 - add topics :
kafka-topics --create --topic topic_name --bootstrap-server localhost:9092
kafka-topics --bootstrap-server localhost:9092 --list
kafka-topics --bootstrap-server localhost:9092 --topic topic_name --describe
kafka-topics --bootstrap-server localhost:9092 --topic topic_name --delete

4 - start producer :
kafka-console-producer --topic topic_name --bootstrap-server localhost:9092
> blablabla

5 - start consumer
kafka-console-consumer --topic topic_name --from-beginning --bootstrap-server localhost:9092
blablabla
kafka-console-consumer --topic topic_name --bootstrap-server localhost:9092

