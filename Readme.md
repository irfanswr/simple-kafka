# Kafka

Foobar is a Python library for dealing with word pluralization.

## Installation

## Format Data Directory

1. Generate uuid:
```
.\bin\windows\kafka-storage.bat random-uuid
```

2. Copy uuid:

```
.\bin\windows\kafka-storage.bat format --cluster-id <uuid> --config config\kraft\server.properties
```

*It will be created file **bootstrap.checkpoint** and **meta.properties**.*

## Running Kafka

```
.\bin\windows\kafka-server-start.bat .\config\kraft\server.properties
```

*Wait until **Kafka Server started**.*