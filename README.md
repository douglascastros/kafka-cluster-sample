## kafka-cluster-sample

### run image

* docker-compose up -d
* docker exec -it kafka-cluster-sample-kafka-1-1 bash

### create topic

* kafka-topics --create --bootstrap-server localhost:19092 --replication-factor 3 --partitions 3 --topic mytopic
* kafka-topics --list --bootstrap-server localhost:19092
* kafka-topics --describe --bootstrap-server localhost:19092 --topic mytopic

### create producer

* kafka-console-producer --broker-list localhost:19092 --topic mytopic

### create consumer

* kafka-console-consumer --bootstrap-server localhost:19092 --topic mytopic
* kafka-console-consumer --bootstrap-server localhost:19092 --topic mytopic --from-beginning
* kafka-console-consumer --bootstrap-server localhost:19092 --topic mytopic --from-beginning --group a