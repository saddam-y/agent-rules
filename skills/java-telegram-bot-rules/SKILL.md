Start:
- Before creating a project, you need to ask what the package will be.

Use kebab-case for keys in aplication.yml.

Use the key word var in init variables.

DB work layer must have dao package and Dao in suffix.

Web:
- Controllers place in controlle package.
- Use static html/css/js and place in resources.

All models place in model package, with additional subpackages.

Stack: Java 21, Gradle, Micronaut, Jdbi, for telegram - rubenlagus/TelegramBots, Flyway, Postgres.

Telegram:
- Use only webhook handler with /webhook path

Add logback.xml and add configs that i can only specify log level if i need it

Add gradle wrapper in root and ./gradlew

---

  Проект-референс: Java Telegram Bot (Micronaut)

  Стек:
  - Java 21
  - Gradle (wrapper)
  - Micronaut (HTTP + DI)
  - JDBI + PostgreSQL
  - Flyway
  - TelegramBots (rubenlagus/webhook mode)

  Структура:
  - `src/main/java/<base-package>/`
  - Пакеты:
    - `controller` — HTTP/webhook контроллеры
    - `service` — бизнес-логика
    - `dao` — доступ к БД (суффикс `Dao`)
    - `model` — доменные модели (с подпакетами по доменам)
    - `config` — конфигурация приложения
    - `bot` — Telegram-бот и клавиатуры
    - `jobs` — фоновые джобы/обработчики
    - `ai` — интеграции AI-провайдеров
    - `exception` — кастомные исключения

  Ресурсы:
  - `src/main/resources/application.yml` (ключи в kebab-case)
  - `src/main/resources/logback.xml`
  - `src/main/resources/db/migration` (Flyway)
  - `src/main/resources/public` (static html/css/js)
  - `src/main/resources/messages.yml`, prompts json

  Тесты:
  - `src/test/java/<base-package>/...` (unit + integration)

  Инфраструктура:
  - `systemd/*.service`, `*.env.example`, `*.nginx.conf`
  - `Makefile` для локального запуска и деплоя

  Telegram-правила:
  - Только webhook-режим
  - Webhook path: `/webhook
