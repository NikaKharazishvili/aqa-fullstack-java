# Java Full-Stack Test Automation Suite

**API • UI • DB** tests across independent Maven + TestNG modules

![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk)
![Maven](https://img.shields.io/badge/Maven-3.9-C71A36?logo=apachemaven)
![TestNG](https://img.shields.io/badge/TestNG-7.x-brightgreen)
![Tools](https://img.shields.io/badge/Tools-Selenium%20·%20REST%20Assured%20·%20MySQL-000000)

---

## Key Features:
- Clean, client-based architecture (reusable API clients, Page Object Model for UI)
- Layered coverage: API, UI, and DB tests as independent Maven modules
- Config-driven (`db.properties`) — swap databases without touching test code
- Includes a Postman collection (`postman-project.json`) for manual API testing alongside the automated suite

---

## Project Structure:
- **APITests/**: REST Assured client for the [Reqres API](https://reqres.in). Covers user CRUD, registration, login, delayed response, and resources, with status code and response body validation
- **DBTests/**: Data integrity tests against a sample `game_accounts` MySQL DB. DB target configurable via `db.properties`; SQL setup script included under `resources`
- **UITests/**: Selenium POM suite for [Practice Automation](https://practice-automation.com/). Organized into TestNG suites with reusable, maintainable components

---

## Run Tests
```bash
mvn test    # Runs everything via testng.xml
```
Each module (`APITests`, `DBTests`, `UITests`) can also be run independently by opening its own `testng.xml`.

**DB setup**: import `game_accounts.sql` (in `resources`) into MySQL, then set the connection URL, username, and password in `db.properties`.

## Important Note
The suite is complete and functional; failures occur due to protections added to public test environments after development, not implementation issues.
- `APITests` worked previously, but `reqres.in` now enforces CAPTCHA, blocking automation.
- `UITests` were stable, but the demo site intermittently returns "Too Many Requests".

## Requirements
- Java 17+ and Maven installed