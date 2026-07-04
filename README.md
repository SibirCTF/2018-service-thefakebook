# 2018-service-thefakebook

Социальная сеть с профилями, друзьями и личными сообщениями.

- **Игра:** Sibir CTF 2018 (2018)
- **Автор:** —
- **Стек:** Python, Django, PostgreSQL, Gunicorn
- **Порт сервиса:** 8000

## Запуск

Подробности — в [`vuln-service/README.md`](vuln-service/README.md). Типовой запуск:

```
cd vuln-service
docker compose up --build -d
```

## Структура репозитория

- `vuln-service/` — уязвимый сервис;
- `checker_thefakebook/` — чекер для жюри ctf01d;
- `README.md` — этот файл.

## Уязвимости

- **Access Control Bypass** (High) — Фильтр сообщений учитывает поле about_me, что позволяет читать чужие переписки.
- **Sensitive Data Exposure** (Medium) — Пароль пользователя сохраняется в cookie passw.
