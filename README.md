# Docker
#### `https://docs.docker.com`

## How to run
```bash
docker compose -f ./postgres.yml up -d
# or
docker compose -f ./<docker_compose_name>.yml --build -d
docker compose -f ./... up down -v
```
### How to log
```bash
docker compose -f ./... logs -f
```

### How to exec
```bash
docker compose -f ./python.yml exec python sh
docker compose -f ./... exec <service_name> bash
```

#### Extra config:
```
services:
  service_name_1:
    deploy:
      replicas: 10
    networks:
      - local_net
    depends_on:
      service_name_2:
        condition: service_healthy
      service_name_3:
        condition: service_healthy
networks:
  local_net:
    external: true
```

#### Structure:
```
├── flower.yml
├── kafka.yml
  ├── config/server.properties
  ├── secrets/kafka_server_jaas.conf
├── metabase.yml
├── minio.yml
├── mongo.yml
├── n8n.yml
├── ollama.yml
├── portainer.yml
├── postgres.yml
  ├── README.md
├── proxy.yml
  ├── config.json
├── python.yml
├── rabbitmq.yml
  ├── rabbitmq.conf
  ├── rabbitmq.conf.example
├── redis.yml
  ├── redis.conf
  ├── redis.conf.example
├── README.md
```
