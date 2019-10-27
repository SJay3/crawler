# Changelog

Каждая версия должна:

- Показывать дату релиза в формате, упомянутом выше.
- Группировать изменения согласно их влиянию на проект следующим образом:
  - [Added] для новых функций.
  - [Changed] для изменений в существующей функциональности.
  - [Deprecated] для функциональности, которая будет удалена в следующих версиях.
  - [Removed] для функциональности, которая удалена в этой версии.
  - [Fixed] для любых исправлений.
  - [Security] для обновлений безопасности.

## [ToDo]
- Create docker-compose.prod.yml for prod env


## [Unreleased]
### Added
- Create docker-compose.stage.yml for stage env

## [0.1.0] 2019-10-18
### Added
- Update readme how to work with gitlab
- Create deploy to stagging
- Create deploy for prod

## [0.0.3] 2019-10-17
### Added
- Create build stage in gitlab-ci

## [0.0.2] 2019-10-16
### Added
- Create docker-compose.yml for crawler
- Create basic .gitlab-ci.yml for pipeline for crawler
- Create test stage in gitlab-ci

## [0.0.1] 2019-10-11
### Added
- Create Dockerfile for crawler-engine
- Create Dockerfile for crawler-ui
- Create docker-compose.yml for local and service testing for crawler-engine
- Create docker-compose.yml for local and service testing for crawler-ui

### [Fixed]
- Update pika to version 1.0.1 in crawler-engine
- Fixed crawler-engine to work with pika 1.0.1. Add `on_message_callback=callback` argument to `basic_consume` function after queue argument instead of using callback before

