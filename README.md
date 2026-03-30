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

## Локальный запуск вместе с monitoring

Из корня репозитория можно поднять приложение и весь observability-стек одной командой:

```bash
docker compose up -d --build
```

После запуска будут доступны:

- API docs: `http://localhost:10004/docs`
- Метрики backend: `http://localhost:10004/metrics`
- Frontend: `http://localhost`
- Prometheus: `http://localhost:9090`
- Grafana: `http://localhost:3000`
- Loki: `http://localhost:3100`
- Alertmanager: `http://localhost:9093`

Grafana login: `admin` / `admin123`.
