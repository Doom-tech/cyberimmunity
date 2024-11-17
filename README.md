# Общая информация

### [Условия задачи](docs/task.md)

### [Отчёт](docs/report.md)

## Оговорка разработчика и условия использования

Применять только в учебных целях. Данный код может содержать ошибки, автор не несёт никакой ответственности за любые последствия использования этого кода.
Условия использования и распространения - GPL лицензия (см. файл [LICENSE](LICENSE)).

### Системные требования

Данный пример разработан и проверен на ОС Ubuntu 24.04, авторы предполагают, что без каких-либо изменений этот код может работать на любых Debian-подобных OS, для других Linux систем. Для MAC OS как минимум необходимо использовать другой менеджер пакетов. В Windows необходимо самостоятельно установить необходимое ПО или воспользоваться виртуальной машиной с Ubuntu (также можно использовать WSL версии не ниже 2).

### Используемое ПО

Стандартный способ запуска демо-версии предполагает наличие установленного пакета *docker* (не ниже 25 версии), а также *docker compose* (входит в стандартный пакет Docker). Для автоматизации типовых операций используется утилита *make*, хотя можно обойтись и без неё, вручную выполняя соответствующие команды из файла Makefile в командной строке.

Другое используемое ПО (в Ubuntu будет установлено автоматически, см. следующий раздел):

- python (желательно версия не ниже 3.8)
- pipenv (для виртуальных окружений python, не ниже 3.8)

Для работы с кодом примера рекомендуется использовать VS Code или PyCharm.

В случае использования VS Code следует установить расширения

- REST client
- Docker
- Python

### Настройка окружения и запуск примера

Подразумевается наличие развернутой по предоставленному образцу машины с установленным и настроенным ПО.

Подготовка среды разработки:

```make dev_install```

Для запуска примера:

```make all```

просмотр логов:

```make logs```

тестирование (будут запущен e2e тест)

``` make test ```

тестирование политик безопасности

``` make test_security ```

завершение работы:

```make clean```
