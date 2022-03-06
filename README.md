# Kafka Tutorial - Spring Boot Microservices

Based on <https://www.youtube.com/watch?v=SqVfCyfCJqw>

**Overview**

![kafka overview](./kafka.png)

**Topics**

![kafka topics](./kafka-topics.png)
![kafka topics](./kafka-topics-partition.png)

**Architecture**

![kafka arch](./kafka-architecture.png)

**Use Case**

![kafka use case](./kafka-use-case.png)

**Capabilities**

<http://kafka.apache.org>

![kafka core capabilities](./kafka-core-capabilities.png)

<https://hellokube.dev/posts/three-ways-zookeepeerless-kafka/>

```bash
podman run -it --name kafka-zkless -p 9092:9092 -e LOG_DIR=/tmp/logs quay.io/strimzi/kafka:latest-kafka-3.1.0-amd64 /bin/sh -c 'export CLUSTER_ID=$(bin/kafka-storage.sh random-uuid) && bin/kafka-storage.sh format -t $CLUSTER_ID -c config/kraft/server.properties && bin/kafka-server-start.sh config/kraft/server.properties'
kafkacat -b localhost -L

```