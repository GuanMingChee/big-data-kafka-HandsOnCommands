# big-data-kafka-HandsOnCommands
`.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties`
<br/>
`.\bin\windows\kafka-server-start.bat .\config\server.properties`
<br/>
`.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic winter-messages`
<br/>
`.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list`
<br/>
`.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic winter-messages`
<br/>
`.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic winter-messages --from-beginning`
