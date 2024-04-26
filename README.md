# docker-compose-applications
Boilerplate docker-compose code for some cool apps. 👊

Version for everything is *latest*, keep up!

## Applications

### Databases
- [Mongo](databases/mongo/docker-compose.yaml)

```bash
docker compose -f databases/mongo/docker-compose.yaml up -d
```

- Redis

```bash
docker compose -f databases/redis/docker-compose.yaml up -d
```

### Message Brokers
- [RabbitMQ](message-brokers/rabbitmq/docker-compose.yaml)

```bash
docker compose -f message-brokers/rabbitmq/docker-compose.yaml up -d
```

- [Kafka (Kraft)](./message-brokers/kafka/docker-compose.yaml)

```bash
docker compose -f message-brokers/kafka/docker-compose.yaml up -d
```


