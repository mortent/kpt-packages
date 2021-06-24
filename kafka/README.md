# Kafka



## Test

Create topic:
k -n foo run --env="KAFKA_CFG_ZOOKEEPER_CONNECT=zookeeper:2181" --image=bitnami/kafka:latest foo -- kafka-topics.sh --create --topic quickstart-events --partitions 2 --replication-factor 1 --zookeeper zookeeper:2181

List topics:
k -n foo run --env="KAFKA_CFG_ZOOKEEPER_CONNECT=zookeeper:2181" --image=bitnami/kafka:latest foo -- kafka-topics.sh --list  --zookeeper zookeeper:2181