### Create Kafka topic:

## Make sure run all this command inside docker kafka container exc tab

kafka-topics --create --topic (topic_name) --bootstrap-server localhost:9092
e.g: kafka-topics --create --topic product --bootstrap-server localhost:9092

List Kafka topics:

kafka-topics --list --bootstrap-server localhost:9092

Get Topic details, partition counts etc.
kafka-topics --describe --bootstrap-server localhost:9092 --topic (topic_name)
e.g: kafka-topics --describe --bootstrap-server localhost:9092 --topic product

Alter the topic, change partition:
kafka-topics --alter --bootstrap-server localhost:9092 --topic (topic_name) --partitions 6
e.g: kafka-topics --alter --bootstrap-server localhost:9092 --topic product --partitions 6

Publish a message to Kafka topic

kafka-console-producer --bootstrap-server localhost:9092 --topic pricing

Check messages in a topic
kafka-console-consumer --bootstrap-server localhost:9092 --topic (topic_name) --from-beginning
e.g kafka-console-consumer --bootstrap-server localhost:9092 --topic product --from-beginning

<

<!--
for go inside docker kafka container:- 

docker exec -it kafka bash

====================
docker compose down
docker rm -f kafka
Remove-Item -Recurse -Force .\kafka-data
docker compose up -d
 -->
