# AGENTS.md

This file tells Codex how to run, test, and contribute to this project.
Monorepo with a **Java Spring Boot** backend and **React + TypeScript** frontend.

---

## Objectives
- Create a working skeleton:
  - **Backend**: Java 21, Spring Boot 3, Gradle, JUnit 5
  - **Frontend**: React, TypeScript, Vite, TailwindCSS, Vitest
- Provide initial endpoints and pages:
  - `GET /api/health` → `{ "status": "ok" }`
  - `POST /api/categorize` → returns mocked categories for an array of transactions
  - Frontend onboarding page that displays 3 example transactions and lets users choose categories
- Include unit tests for backend (JUnit) and frontend (Vitest).

---

## How to Run (local)
### Backend
```bash
cd backend
./gradlew bootRun

Runs on: http://localhost:8080

## How to Test
## Backend (JUnit 5)

cd backend
./gradlew test


## Frontend (Vitest)
cd frontend
npm test


Conventions

Backend

Java 21, Spring Boot 3, Gradle (Kotlin DSL or Groovy—either is fine)

Package root: com.example.finance

REST endpoints under /api/*

Controllers in api/, services in service/, DTOs in domain/

Use Jackson for JSON; validate inputs

Enable CORS for http://localhost:5173 in dev

Frontend

React + TypeScript

Vite for dev/build; TailwindCSS for styling

Place reusable UI in src/components/

Keep an src/lib/api.ts helper for HTTP calls; read base URL from VITE_API_URL (fallback to relative)

General

Small, focused commits with descriptive messages

Include tests alongside new code

Keep code simple and production-expandable

Project Layout
/backend
  src/main/java/com/example/finance/...
  src/test/java/com/example/finance/...
/frontend
  src/...
README.md        # root overview
AGENTS.md        # this file

Initial Contracts
Backend Endpoints

GET /api/health
Response:

{ "status": "ok" }


POST /api/categorize
Request (array of transactions):

[
  { "merchant": "Chipotle", "amount": 14.25 }
]


Response (mocked categories):

[
  { "merchant": "Chipotle", "amount": 14.25, "category": "FOOD" }
]

Frontend Page

/onboarding

Renders 3 example transactions

Each row has a category dropdown: FOOD | RENT | INCOME | OTHER

“Submit” button that:

If backend is running: POSTs to /api/categorize

Otherwise: uses a mocked client-side function

Tasks for Codex (first pass)

Backend scaffold

Create Spring Boot app with GET /api/health and POST /api/categorize

Add DTOs for request/response

Add JUnit tests for both endpoints

Add simple CORS config for http://localhost:5173 (dev only)

Frontend scaffold

Create React+TS Vite app with Tailwind

Add /onboarding page with 3 example transactions and category dropdowns

Add lib/api.ts with health() and categorize() (supports mock mode)

Add a Vitest test that renders onboarding and changes one category

Quality

Ensure both projects run locally with the commands above

Ensure all tests pass with the commands above

Environment

Frontend: optional .env with VITE_API_URL=http://localhost:8080

Backend: default profile only; no DB required in this phase

Success Criteria

./gradlew bootRun serves endpoints and passes tests

npm run dev serves the onboarding page; test passes

Code and tests are small, idiomatic, and easy to extend


