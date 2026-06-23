# Docker

## How to run
```bash
docker compose -f postgres.yml up
# or
docker compose -f ./... up --build -d
docker compose -f ./... down -v
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
├── metabase.yml
├── minio.yml
├── mongo.yml
├── n8n.yml
├── ollama.yml
├── portainer.yml
├── postgres.yml
├── proxy.yml
  ├── config.json
├── python.yml
├── rabbitmq.yml
  ├── rabbitmq.conf
  ├── rabbitmq.conf.example
├── redis.yml
  ├── redis.conf
  ├── redis.conf.example
```
