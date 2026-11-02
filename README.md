# Todo REST API — FastAPI, PostgreSQL & Docker

[![CI — FastAPI Test Suite & Coverage](https://github.com/felipegtech/Todo-REST-API/actions/workflows/ci.yml/badge.svg)](https://github.com/felipegtech/Todo-REST-API/actions/workflows/ci.yml)

Production-structured RESTful API built with **FastAPI**, **SQLAlchemy**, and **PostgreSQL**, featuring layered architecture (`routes` → `services` → `repositories`), external REST API integration, Docker Compose orchestration, and automated `pytest` test suites.

---

## Key Features
- **Layered Backend Architecture:** Clean separation between HTTP routes, business logic services, and SQLAlchemy data repositories.
- **Full CRUD & Filtering:** Complete note lifecycle management with Pydantic schema validation.
- **External API Integration:** Asynchronous/HTTPX integration with external user & post providers.
- **Containerized Infrastructure:** Ready-to-run `Dockerfile` and `docker-compose.yml` with PostgreSQL.
- **Automated CI & Testing:** Unit and integration tests (`test_routes.py`, `test_services.py`, `test_external.py`) executed automatically on every push via GitHub Actions.

---

## Quick Start (Docker Compose)

```bash
cd todo-api
cp .env.example .env
docker compose up --build
```

- **Interactive Swagger UI:** `http://localhost:5000/docs`
- **Detailed API Reference:** See [todo-api/README.md](./todo-api/README.md)

## Running Tests Locally

```bash
cd todo-api
DATABASE_URL="sqlite:///./test.db" pytest -v --cov=app
```
