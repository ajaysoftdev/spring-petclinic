# ADR 0003: Maven Wrapper as Initial Build Path

- Status: Proposed developer workflow

## Context
Maven and Gradle wrappers and build definitions are present. A developer machine may not have either tool installed globally.

## Decision
Use the checked-in Maven Wrapper as the initial onboarding path because it avoids a separate global Maven installation. Gradle remains available.

## Consequences
- A compatible JDK is still required.
- Wrapper configuration remains version controlled.
- Commands must be tested locally before being marked verified.
- This does not remove Gradle support.
