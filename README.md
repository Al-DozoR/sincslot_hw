# SincSlot

Веб-приложение для онлайн-записи клиентов в компанию.

## Текущий статус

В репозитории настроены локальные проверки через `pre-commit` и CI-пайплайн GitHub Actions для Pull Request в `main`.

- Конфигурация CI: [`.github/workflows/ci.yml`](.github/workflows/ci.yml)
- Документация по пайплайну: [`docs/ci_pipeline_logic.md`](docs/ci_pipeline_logic.md)
- Документация по git hooks: [`docs/git_hooks_config.md`](docs/git_hooks_config.md)

## Стек

### Frontend

- JavaScript
- React
- Vite

### Backend

- Python
- FastAPI
- PostgreSQL

## Что проверяет CI

- `Lint`: `eslint`, `prettier`, проверки `pre-commit`
- `Test`: `pytest` с PostgreSQL test DB
- `Security`: `bandit` и `gitleaks`
- `Notify`: уведомление в Telegram при наличии секретов

## Скриншоты пайплайна

Сейчас подключены placeholder-изображения. После первого реального запуска GitHub Actions замени их на свои скриншоты.

![Green build](docs/artifacts/pipeline_success_example.png)
![Failed build](docs/artifacts/pipeline_fail_example.png)

## Сравнение с VSM из ДЗ 201

Если в AS-IS этапе ручная проверка и прогон занимали `2-4 часа`, то с `pre-commit` и CI обратная связь приходит за `5-10 минут`.

Это значит, что этап проверки теперь занимает примерно `4-8%` от исходного времени, а экономия составляет порядка `92-96%`.
