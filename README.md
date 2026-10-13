# MarketPro V75.1 — runnable build

MarketPro is a digital-marketing operating system foundation with persistent PostgreSQL data, workspace-isolated JWT authentication, campaign management, lead pipeline, strategy library, approval controls, audit events and an AI provider boundary.

## Run with Docker

```bash
docker compose up --build
```

- Web: http://localhost:5173
- API docs: http://localhost:8000/docs
- Health: http://localhost:8000/health

The first login can create a workspace automatically. Use a password of at least 6 characters.

## Local development

Backend:
```bash
cd backend
pip install -r requirements.txt
DATABASE_URL=postgresql+psycopg://marketpro:marketpro@localhost:5432/marketpro uvicorn app.main:app --reload --port 8000
```

Frontend:
```bash
cd frontend
npm install
npm run dev
```

## V75.1 completed in this package

- PostgreSQL-backed persistence via SQLAlchemy
- PBKDF2 password hashing and JWT sessions
- Workspace isolation on all business records
- Campaign create/list/status workflow
- Lead create/list/status workflow
- Strategy create/list workflow
- Approval create/list/approve/reject workflow
- Audit event logging
- Business Brain persistence
- AI brief adapter boundary
- Responsive React command center
- Docker Compose with PostgreSQL + Redis + API + web
- Health and system-status endpoints

## Production hardening still required before public launch

Configure a strong secret, managed PostgreSQL/Redis, HTTPS, real AI/provider credentials, external marketing connectors, background workers, rate limiting, backups, monitoring and a CI/CD deployment target.
