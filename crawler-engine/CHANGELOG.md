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

- Create basic .gitlab-ci.yml for pipeline

## [Unreleased]

## [0.0.1] 2019-10-10
### Added
- Create Dockerfile
- Create docker-compose.yml for local and service testing

### [Fixed]
- Update pika to version 1.0.1
- Fixed crawler to work with pika 1.0.1. Add `on_message_callback=callback` argument to `basic_consume` function after queue argument instead of using callback before
