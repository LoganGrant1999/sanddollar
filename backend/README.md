Backend – Spring Boot (Java)
Java 21 + Spring Boot 3 backend service for the Personal Finance AI app.

Run
To run the backend service, use the following command:

./gradlew bootRun

The backend will be available at http://localhost:8080.

Endpoints
GET /api/health
This endpoint checks the health of the service.

Response:

{ "status": "ok" }

POST /api/categorize
This endpoint categorizes financial transactions.

Request:

[{ "merchant": "Chipotle", "amount": 14.25 }]

Response (mocked):

[{ "merchant": "Chipotle", "amount": 14.25, "category": "FOOD" }]

Tests
To run the tests, use the following command:

./gradlew test

JUnit 5 is used for unit and integration tests.

Source Code and Tests Location
Source code: src/main/java/com/example/finance

Tests: src/test/java/com/example/finance
