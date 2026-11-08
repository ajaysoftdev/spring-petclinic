# Threat Model: Spring PetClinic

- Status: Starter; assessment pending
- Scope: Browser-facing Spring MVC application and configured databases

## 1. Assets
Owner contact information, pet/visit records, database credentials, application configuration, availability and build artifacts.

## 2. Entry points
Browser form submissions, application-to-database connections, Actuator/management endpoints, build workflows and local database consoles.

## 3. Threat register

| Threat | Potential impact | Controls to verify |
|---|---|---|
| Forged state-changing request | Unauthorised modification | CSRF and session/origin behaviour |
| Malformed form input | Data integrity / errors | Server validation and safe binding |
| SQL injection | Data disclosure/modification | Parameterised repository access |
| Exposed management endpoint | Operational information disclosure | Endpoint exposure and authentication |
| Leaked DB credential | Data compromise | Secret handling and least privilege |
| Personal data in logs | Privacy exposure | Redaction and minimisation |
| Vulnerable dependency | Application compromise | Dependency scanning and patching |
| Over-permissive CI token | Supply-chain compromise | Workflow permissions |

## 4. Assessment
Rate likelihood and impact only after inspecting actual controls and deployment context. Record evidence, mitigation, owner role and residual risk.

## 5. Verification
Inspect web/security configuration, controller binding, repository queries, Actuator settings, application properties and CI workflows. Use synthetic data.

## 6. Limitations
This is a threat-discovery starter, not a penetration test or completed STRIDE assessment. Do not report vulnerabilities without evidence.
