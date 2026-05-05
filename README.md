# Log Anomaly Detection Platform

End-to-end log anomaly detection platform using **Laravel** (API and orchestration), **React** (dashboard and operator UI), and **Python** (ML inference and training pipelines).

This repository is being built incrementally. Step 1 establishes folders, Docker Compose, and shared configuration only; application code for each stack arrives in later steps.

## Repository layout

| Path | Purpose |
|------|---------|
| `backend/` | Laravel API, authentication, ingestion hooks, and integration with Postgres/Redis/ML service. |
| `frontend/` | React SPA for visualization, alerts, and configuration. |
| `ml-service/` | Python service for feature extraction, scoring, and model lifecycle. |
| `database/` | SQL migrations, seeds, and optional `init` scripts mounted into Postgres. |
| `docker/` | Nginx and other container configuration not tied to a single app. |
| `docs/` | Architecture notes, runbooks, and API documentation. |
| `samples/` | Example log files and fixtures for local testing. |
| `.github/workflows/` | CI/CD pipelines (tests, lint, images). |
| `docker-compose.yml` | Local orchestration: backend, frontend, ML service, Postgres, Redis, Nginx. |
| `.env.example` | Template environment variables for Compose and apps. |

## Quick start (Docker)

1. Optional: copy `cp .env.example .env` (PowerShell: `Copy-Item .env.example .env`) so Compose and tools pick up shared variables; edit secrets (especially `POSTGRES_PASSWORD`).
2. From the repo root: `docker compose up --build`.

Nginx listens on `NGINX_PORT` (default `80`). Stub containers are used for backend, frontend, and ML until those stacks are implemented in later steps.

## Requirements

- Docker Engine and Docker Compose v2

## License

Specify your license in a later step when you finalize project governance.
