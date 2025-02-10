# Zookeeper related actions and commands

1. To start zookeeper service run the following command in the terminal:

`brew services start zookeeper`

You will be seeing this `homebrew.mxcl.zookeeper` in the terminal.

2. To confirm the status on zookeeper, go to the folder `/opt/homebrew/bin` and `double-click` the `zkCli.sh` file, in terminal you will be seeing

```js
Connecting to localhost:2181
Welcome to ZooKeeper!
JLine support is enabled
```

3. To re-start zookeeper service run the following command in the terminal:

`brew services restart zookeeper`

4. Location of Zookeeper configurations will be in

`opt/homebrew/etc/zookeeper`

5. Zookeeper properties will be find in below `path/file`

`opt/homebrew/etc/kafka/zookeeper.properties`

6. To stop zookeeper service run the following command in the terminal:

`brew services stop zookeeper`
