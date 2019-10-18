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

## Пайплайн гитлаба

Проверим, что в репозитории или группе crawler в гитлабе, существуют переменные:
- `CI_REGISTRY_USER` - логин на dockerhub
- `CI_REGISTRY_PASSWORD` - пароль от dockerhub

Добавляем remote к репозиторию:

```shell
git remote add gitlab http://<gitlab_ip>/crawler/crawler.git
```

Пушим изменения

```shell
# Ветка dev
git push gitlab dev:dev

# Ветка master
git push gitlab master

```

Юнит тесты и сборка запускаются автоматически.
На stage и prod - ручной запуск. На stage разрешается разворачивать ветки dev и master. На prod - только теги, поэтому при мерже в мастер обязательно выставление тегов.
