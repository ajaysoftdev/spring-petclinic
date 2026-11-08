# Testing Guide

## 1. Existing test layout
The test source tree includes model, owner, service, system and vet packages. Top-level integration classes include PetClinicIntegrationTests, MySqlIntegrationTests, PostgresIntegrationTests and PetClinicConcurrencyTests. Inspect test methods before making coverage claims.

## 2. Maven commands

    ./mvnw test
    ./mvnw verify

Windows PowerShell:

    .\mvnw.cmd test
    .\mvnw.cmd verify

## 3. Build quality configuration
The Maven build configures Java version enforcement, Spring Java Format validation, Checkstyle/no-HTTP checks and JaCoCo reporting. Exact phases and outputs are in pom.xml.

## 4. Database integration
The repository declares Testcontainers-related dependencies and database-specific integration test classes. Confirm Docker availability and prerequisites before running.

## 5. Feature test matrix
For owner, pet and visit changes cover valid form submission, required fields, format validation, unknown references, persistence relationships, error rendering and supported database profiles.

## 6. Evidence
Record commit, JDK, command, exit code, test count and failures. Do not claim a suite passed unless executed.
