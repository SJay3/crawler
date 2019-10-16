# README

Микросервисное приложение crawler для проекта otus devops.

Состоит из:
- engine
- ui

Дополнительные компоненты:
- mongodb
- rabbitmq

## Сборка контейнеров

```shell
export USER_NAME=<docker_hub_username>
# engine
cd crawler-engine && docker build -t $USER_NAME/crawler-engine .

# ui
cd crawler-ui && docker build -t $USER_NAME/crawler-ui .
```

## Локальное тестирование

```shell
docker-compose up -d
```
