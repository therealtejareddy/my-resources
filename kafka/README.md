## steps

1. start zookeeper

2. start kafka-server
3. create topic
4. start producer
5. start consumer

## commands
#### start zookeeper

`bin/zookeeper-server-start.sh config/zookeeper.properties`

#### start kafka server
`bin/kafka-server-start.sh config/server.properties`

#### create topic
`bin/kafka-topics.sh --create --topic demo_testing2 --bootstrap-server {Put the Public IP:9092} --replication-factor 1 --partitions 1`

`bin/kafka-topics.sh --create --topic demo_testing2 --bootstrap-server {Put the Public IP:9092} --replication-factor 1 --partitions 1 --if-not-exists`

#### start producer
`bin/kafka-console-producer.sh --topic demo_testing2 --bootstrap-server {Put the Public IP:9092}`

#### start consumer
`bin/kafka-console-consumer.sh --topic demo_testing2 --bootstrap-server {Put the Public IP:9092}`

#### list topics
`bin/kafka-topics.sh --list --bootstrap-server localhost:9092`

# kafka download
`wget https://downloads.apache.org/kafka/3.3.1/kafka_2.12-3.3.1.tgz`

`tar -xvf kafka_2.12-3.3.1.tgz`