# Functionality Execution

### Create a Kafka topic

`/opt/homebrew/bin/kafka-topics --create --topic test-topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1`
Result: `Created topic test-topic.` if not already exists.

### Run a Kafka Producer

Publishing the message/data to the Topics after running this command.

`/opt/homebrew/bin/kafka-console-producer --topic test-topic --bootstrap-server localhost:9092`

Sent message:

```js
hellow;
world;
```

### Run a Kafka Consumer

Receiving the message/data from the Topics published by producer after running this command.

`/opt/homebrew/bin//kafka-console-consumer --topic test-topic --bootstrap-server localhost:9092 --from-beginning`

Received message:

```js
hellow;
world;
```

### Create a Kafka topic with multiple partitions

`/kafka-topics.sh --create --topic test-topic-two --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3` # it will throw error if topic is already there
