# SincSlot

Веб-приложение для онлайн-записи клиентов в компанию.

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
