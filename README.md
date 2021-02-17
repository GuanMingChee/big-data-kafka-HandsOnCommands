# big-data-kafka-HandsOnCommands

Use PowerShell to run the commands below. Make sure your PowerShell is at your kafka directory path (recommended path is C:\kafka_version).
<br/>
<br/>
To start Zookeeper, please run the command below (closing the Powershell window indicate ending Zookeeper):
<br/>
`.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties`
<br/>
<br/>
To start Kafka, please run the command below (closing the Powershell window indicate ending Kafka):
<br/>
`.\bin\windows\kafka-server-start.bat .\config\server.properties`
<br/>
<br/>
To create/delete/list topics, please run the commands below (change the command to --delete for delete purpose):
`.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic winter-messages`
<br/>
`.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list`
<br/>
<br/>
To run Kafka Producer (write input), please run the command below (a '>' will appear indicating awaiting input):
`.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic winter-messages`
<br/>
The prompt will run as long as you you do not terminate the job.
<br/>
<br/>
To run Kafka Consumer (display input entered using Kafka Producer), please run the command below (output instantly when there is new input):
`.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic winter-messages --from-beginning`
<br/>
The prompt will run as long as you you do not terminate the job.
