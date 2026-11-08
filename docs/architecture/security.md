# Security Architecture: Spring PetClinic

- Status: Review guidance; not a completed security audit

## 1. Scope
Identify areas requiring inspection. This document does not claim each control is verified or that the application is production-ready.

## 2. Web controls
Review input validation, server-side binding, Thymeleaf output escaping, CSRF protection, session/cookie settings, error pages, exception handling, Actuator exposure and request/resource limits. A dependency declaration alone does not prove effective configuration.

## 3. Database controls
Use least-privilege database accounts, isolate test and production data, restrict database network access, use encrypted transport where supported and avoid logging personal data in SQL parameters.

## 4. Personal data
Owner contact details should be treated as personal data. Use synthetic records in portfolio examples and screenshots.

## 5. Supply chain
Review dependency versions, Maven/Gradle plugins, wrapper distribution settings, container base images and GitHub Actions permissions. Record scan output and date when a scan is performed.

## 6. Verification checklist
Validate malformed/oversized forms, verify CSRF behaviour, check error disclosure, inspect actuator exposure, check for committed credentials and review dependency/workflow changes.

## 7. Status
Security review has not yet been executed. Record findings with reproduction, severity, affected code and remediation evidence.
