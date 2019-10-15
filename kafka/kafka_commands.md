# Kafka Commands


## Run Kafka (After installing from brew)
`zookeeper-server-start /usr/local/etc/kafka/zookeeper.properties & kafka-server-start /usr/local/etc/kafka/server.properties`

## Creating a Topic
`kafka-topics --create --bootstrap-server {bootstrap-server or localhost:9092} --replication-factor 1 --partitions 1 --topic {topic-name}`

## Open up a producer in Terminal
`kafka-console-producer --broker-list {ex. localhost:9092} --topic {topic-name}`

## Open up a consumer in Terminal
`kafka-console-consumer --bootstrap-server {ex. localhost:9092} --topic {topic-name} --from-beginning`

## Delete a topic
`kafka-topics --zookeeper {ex. localhost:2181} --delete --topic {topic-name}`

## Flush a topic
First set retention rate to 1s: `kafka-topics --zookeeper {ex. localhost:2181} --alter --topic {topic-name} --config retention.ms=1000`
Second set retention rate back: `kafka-topics --zookeeper {ex. localhost:2181} --alter --topic {topic-name} --config retention.ms=604800000`

## Create a Consumer group
`kafka-console-consumer --bootstrap-server {ex. localhost:9092} --topic {topic-name} --consumer-property group.id={name-of-consumer-group}`

## Print Consumer group configurations
`kafka-consumer-groups --bootstrap-server {ex. localhost:9092} --describe --group {name-of-consumer-group}`

## List all topics
`kafka-topics --list --zookeeper {ex. localhost:2181}`

## Get details about specific topics
`kafka-topics --describe --zookeeper {ex. localhost:2181} --topic {topic-name}`
