# Working/Testing setup

### Setup Single Broker Cluster of Kafka

**Note:** If Zookeeper & Kafka is already running please ignore Step 1 & Step 2.

Step 1: Start Zookeeper
Open a new terminal and run the following command:

`/opt/homebrew/bin/zookeeper-server-start /opt/homebrew/etc/kafka/zookeeper.properties`
or
`brew services start zookeeper`

Step 2: Start Kafka Brokers
To start a local instance (single Broker Cluster) of Kafka, run the following command:

`/opt/homebrew/bin/kafka-server-start /opt/homebrew/etc/kafka/server.properties`
or
`brew services start kafka`

### Setup Multi Broker Cluster of Kafka

Step 1: To setup multiple kafka servers copy the default server properties to create configurations for each brokers with below command.

```js
cp /opt/homebrew/etc/kafka/server.properties /opt/homebrew/etc/kafka/server-1.properties
cp /opt/homebrew/etc/kafka/server.properties /opt/homebrew/etc/kafka/server-2.properties
```

Step 2: After creating multiple servers, update the configs as below for each files.

**File: server-1.properties**

```js
broker.id=1
listeners=PLAINTEXT://:9093    // -- uncomment the listeners
log.dirs=/opt/homebrew/var/lib/kafka-logs-1 // --add additional folder for separate log tracking
```

**File: server-2.properties**

```js
broker.id=2
listeners=PLAINTEXT://:9094   // -- uncomment the listeners
log.dirs=/opt/homebrew/var/lib/kafka-logs-2 // --add additional folder for separate log tracking
```

Step 3: Start Zookeeper if already not started
Open a new terminal and run the following command:

`/opt/homebrew/bin/zookeeper-server-start /opt/homebrew/etc/kafka/zookeeper.properties`
or
`brew services start zookeeper`

Step 4: Start Kafka Brokers
To start a first broker of Kafka by running any of the following command:

`/opt/homebrew/bin/kafka-server-start /opt/homebrew/etc/kafka/server.properties`
or
`brew services start kafka`

To start Broker 2, run the following command:
`/opt/homebrew/bin/kafka-server-start /opt/homebrew/etc/kafka/server-1.properties`

To start Broker 3, run the following command:
`/opt/homebrew/bin/kafka-server-start /opt/homebrew/etc/kafka/server-2.properties`
