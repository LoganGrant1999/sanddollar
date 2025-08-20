# Personal Finance AI (Java + React)

A budgeting and transaction-categorization app.  
This repository contains both the **backend** (Java Spring Boot) and **frontend** (React + TypeScript).  
Phase 1 provides a working skeleton; later you can add authentication, bank API integration, and AI-powered financial advice.

## Stack
- **Backend:** Java 21 · Spring Boot 3 · Gradle · JUnit 5
- **Frontend:** React · TypeScript · Vite · TailwindCSS · Vitest

## Run
### Backend
```bash
cd backend
./gradlew bootRun
Backend will be available at http://localhost:8080

Frontend
bash
Copy
Edit
cd frontend
npm install
npm run dev
Frontend will be available at http://localhost:5173

Tests
Backend
bash
Copy
Edit
cd backend
./gradlew test
Frontend
bash
Copy
Edit
cd frontend
npm test
Project Structure
bash
Copy
Edit
/backend    # Spring Boot backend (controllers, services, tests)
/frontend   # React frontend (pages, components, tests)
README.md   # Root project overview (this file)
AGENTS.md   # Instructions for Codex
Endpoints (initial backend)
GET /api/health → { "status": "ok" }

POST /api/categorize
Request:

json
Copy
Edit
[{ "merchant": "Chipotle", "amount": 14.25 }]
Response (mocked):

json
Copy
Edit
[{ "merchant": "Chipotle", "amount": 14.25, "category": "FOOD" }]
Next Steps
Add categorization logic with GPT

Persist transactions and budgets (Postgres + JPA)

Build budget dashboard and chat UI

Add authentication
