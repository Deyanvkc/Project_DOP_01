# Popeye

Epitech DevOps project: containerize a multi-service voting application with Docker Compose.

## Local setup

1. Copy the environment template:

```bash
cp .env.example .env
```

2. Replace the placeholder database password in `.env`.
3. Start the stack:

```bash
docker compose -f compose.yml up --build
```

`.env` is intentionally ignored and must never be committed. `.env.example` contains only non-sensitive example values.
