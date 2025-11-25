# Docker

## How to run
```bash
docker compose -f postgres.yml up
# or
docker compose -f ./... up --build -d
docker compose -f ./... down -v
```

#### Structure :
```
├── flower.yml
├── minio.yml
├── ollama.yml
├── portainer.yml
├── postgres.yml
├── rabbitmq.yml
  ├── rabbitmq.conf
  ├── rabbitmq.conf.example
├── redis.yml
  ├── redis.conf
  ├── redis.conf.example
```
