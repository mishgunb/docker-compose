# Docker Compose (nginx + PostgreSQL)

## Структура проекта

```
docker-compose-task/
├── Dockerfile
├── docker-compose.yml
├── .env
├── nginx-config/default.conf
└── html/index.html
```

## Команды для запуска и проверки

```bash
cd docker-compose-task

# собрать образ web и запустить оба контейнера
docker compose up -d --build

# убедиться, что db и web запущены
docker compose ps

# открыть в браузере http://localhost:8080 — должна открыться index.html

# проверить, что данные БД лежат на хост-машине
ls ./pgdata

# остановить контейнеры
docker compose down
```
