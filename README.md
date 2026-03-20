# 🗂️ Task Manager API — Production-Grade Backend

A fully production-ready **FastAPI-based Task Manager API** featuring:
- JWT Authentication
- Async SQLAlchemy ORM
- Alembic Migrations
- Observability (Logs + Prometheus Metrics)
- Docker & Docker Compose Support
- GitHub Actions CI/CD
- GitLab CI compatibility
- DockerHub Auto-build Support
- Unit Tests (pytest + HTTPX)
- Example Data Files

---
## 🚀 Features
- **User Authentication** using JWT (Register/Login)
- **Task CRUD** (Create, List, Update, Delete)
- **Async SQLAlchemy ORM** with SQLite
- **Prometheus Metrics** (`/metrics`)
- **Health Check** Endpoint (`/health`)
- **Fully dockerized** environment
- **Complete CI/CD pipeline**

---
## 📁 Project Structure
```
app/
  ├── main.py
  ├── database.py
  ├── models.py
  ├── schemas.py
  ├── auth.py
  ├── routers_auth.py
  ├── routers_tasks.py
  ├── observability.py
  ├── metrics.py
examples/
tests/
Dockerfile
docker-compose.yml
alembic/
.github/workflows/ci.yml
```

---
## 🐳 Run with Docker
```
docker compose up --build
```
The API starts at:
```
http://localhost:8000
```
Docs:
```
http://localhost:8000/docs
```

---
## 🧪 Run Tests
```
pytest
```

---
## 📊 Monitoring
### Prometheus
```
http://localhost:8000/metrics
```

### Grafana
Import dashboard JSON provided in `task_api_monitoring` module.

---
## 🔑 Authentication Flow
1. Register: `POST /auth/register`
2. Login: `POST /auth/login`
3. Use Bearer token for all task endpoints

---
## 📦 Example Data
Located inside `examples/` folder:
- users_seed.json
- tasks_seed.json
- .env.example
- http_examples.rest

---
## 🔧 CI/CD Pipelines
GitHub Actions workflow included at:
```
.github/workflows/ci.yml
```

GitLab CI compatible pipeline included as `.gitlab-ci.yml`.

DockerHub auto-build instructions provided.

---
## 📝 License
MIT
