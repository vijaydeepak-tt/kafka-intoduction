# Kafka related actions and commands

**Note:** Please confirm Zookeeper instance is running b4 starting the kafka.

1. To start kafka service run the following command in the terminal:

`brew services start kafka`

You will be seeing this `homebrew.mxcl.kafka` in the terminal.

2. To confirm the status on kafka, run the following command in the terminal that lists all the topics available in kafka server. `9092` is default server that kafka runs.

`/opt/homebrew/bin/kafka-topics --list --bootstrap-server localhost:9092`

3. To re-start kafka service run the following command in the terminal:

`brew services restart kafka`

4. Location of Kafka configurations will be in

`/opt/homebrew/etc/kafka`

5. Location of Kafka `log.dirs` config will be set to below path by default

`/opt/homebrew/var/lib/kafka-logs`

6. Kafka properties will be find in below `path/file`

`/opt/homebrew/etc/kafka/server.properties`

7. To stop kafka service run the following command in the terminal:

`brew services stop kafka`
