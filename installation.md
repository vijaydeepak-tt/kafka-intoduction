# Installing Kafka with brew

Step 1: Run brew command for Kafka:
Run the following command which will install Kafka in the terminal.
`brew install kafka`

Step 2: Start the zookeeper services:
The next step is to start the zookeeper services, To start this service run the following command in the terminal:

`brew services start zookeeper`

Step 3: Start the Kafka package:
The next step now is to install the Kafka package, for this type the following command in the terminal and it will start the Kafka services:

`brew services start kafka`

Step 4: Get the $PATH location for the brew:
After performing the above steps, it is important to get the path address for the next steps, by entering a simple echo command mentioned below:

`echo $PATH`

Step 5: Check Kafka topics:
The next step is to check whether the Kafka topics are being displayed by the terminal or not, for doing this run the command on your terminal:

`/opt/homebrew/bin/kafka-topics`

**Note:** Your echo PATH address may change depending on where the homebrew is installed so keep it in mind and change the command accordingly.

Step 6: Start the bootstrap server on localhost:
After completing all of the above steps, it is now time to start the localhost server on the specific port that can be easily used by the Kafka package, for this run the following command in the terminal:

`/opt/homebrew/bin/kafka-topics --list --bootstrap-server localhost:9092`

This will give the following output: "test-kafka"
