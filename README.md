# AQA Fullstack Java

A collection of Java test automation projects (Maven + TestNG), covering API, database, and UI testing.

## Projects

### [APITests](APITests) — REST Assured API Testing
- **Tools/Tech**: Java (OOP), REST Assured, TestNG, Maven
- **Description**: API test automation for the public [Reqres API](https://reqres.in), demonstrating REST API testing skills.
- **Highlights**:
  - Clean client-based structure for reusability
  - Comprehensive test coverage for user CRUD, registration, login, delayed response, and resources
  - Robust validation of status codes and response bodies
- **Setup**: Run tests via `testng.xml`. Includes a `postman-project.json`, importable into Postman for manual API testing.

### [DBTests](DBTests) — Database Testing
- **Tools/Tech**: Java, MySQL, TestNG, Maven
- **Description**: A database testing project designed to retrieve and assert database information.
- **Highlights**:
  - Supports testing with MySQL and other databases via configuration
  - Includes a sample `game_accounts.sql` for database setup
  - Configurable through `db.properties` for flexibility
- **Setup**:
  - Import `game_accounts.sql` (in resources) into your MySQL server.
  - Edit `db.properties` with the appropriate database URL, username, and password.
  - Run tests via `testng.xml`.
- **Note**: Works with other databases if `db.properties` and the SQL in `DatabaseTest.java` are adapted to the new dialect.

### [UITests](UITests) — Selenium UI Testing
- **Tools/Tech**: Java (OOP, POM), Selenium, TestNG, Maven
- **Description**: Automated test cases for [Practice Automation](https://practice-automation.com/), demonstrating Selenium automation skills.
- **Highlights**:
  - Clean Page Object Model structure for reusability
  - Organized with TestNG suites for test execution
  - Maintainable code with reusable components
- **Setup**: Run tests via `testng.xml`.

## Requirements
- Java and Maven installed