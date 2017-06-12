# Kafka Compose

Create a topic: 
```
docker-compose run --rm kafka kafka-topics.sh --create --topic test --replication-factor 1 --partitions 1 --zookeeper zookeeper:2181
```
Start a producer:
```
docker-compose run --rm kafka kafka-console-producer.sh --topic test --broker-list kafka:9092
```
Start a consumer: 
```
docker-compose run --rm kafka kafka-console-consumer.sh --topic test --from-beginning --bootstrap-server kafka:9092
```

## Base image
`ches/kafka`