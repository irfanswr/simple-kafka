# Kafka

Foobar is a Python library for dealing with word pluralization.

## Installation

### Format Data Directory

1. Generate uuid:
```
.\bin\windows\kafka-storage.bat random-uuid
```

2. Copy uuid:

```
.\bin\windows\kafka-storage.bat format --cluster-id <uuid> --config config\kraft\server.properties
```

*It will be created file **bootstrap.checkpoint** and **meta.properties**.*

### Running Kafka

```
.\bin\windows\kafka-server-start.bat .\config\kraft\server.properties
```

*Wait until **Kafka Server started**.*

## Topic

1. Create new topic send message:

```
.\bin\windows\kafka-topics.bat --create --topic uji-coba --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
```

2. Show list topic:

```
.\bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092
```

3. Run procedure (send message):
```
.\bin\windows\kafka-console-producer.bat --topic uji-coba --bootstrap-server localhost:9092
```

4. *Type your message*

5. Open new terminal (receive message):

```
.\bin\windows\kafka-console-consumer.bat --topic uji-coba --from-beginning --bootstrap-server localhost:9092
```
