# Operations Guide

- Status: Operational checklist; deployment not verified

## 1. Runtime
The repository declares Spring Boot Actuator. Exact management endpoints and exposure settings must be verified from configuration and a running instance.

## 2. Readiness
Establish liveness/readiness behaviour, database checks, startup/shutdown, log format/retention, error/latency signals and resource thresholds.

## 3. Database
Default H2 mode is in-memory. For MySQL/PostgreSQL define backup, restore, schema compatibility, connection pool and credential rotation procedures.

## 4. Release readiness
Build and test cleanly, record artifact and source commit, review dependency/security findings, externalise secrets, confirm database profile, verify health checks and rollback, and exclude personal data from logs.

## 5. Incident response
Capture timestamp, environment, release, request details and first causal error. Protect sensitive data. Recover using tested rollback/recovery and record follow-up actions.

## 6. Status
No production deployment, monitoring dashboard, alert configuration or recovery test is claimed.
