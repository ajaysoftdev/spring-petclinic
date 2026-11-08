# Configuration Guide

## 1. Configuration files
- src/main/resources/application.properties
- src/main/resources/application-mysql.properties
- src/main/resources/application-postgres.properties

The active Spring profile selects database-specific configuration. Inspect current files before changing property names or defaults.

## 2. Default local mode
Upstream documentation describes H2 in-memory mode as the default. Data is recreated when the application starts.

## 3. MySQL and PostgreSQL
Drivers and profile-specific settings are present. Setup instructions and SQL scripts are under src/main/resources/db/mysql and src/main/resources/db/postgres.

Use local credentials only. Never commit real passwords or production connection strings.

## 4. Change checklist
Check impact across profiles, secret externalisation, safe defaults, connection/timeout settings, integration coverage and rollback.
