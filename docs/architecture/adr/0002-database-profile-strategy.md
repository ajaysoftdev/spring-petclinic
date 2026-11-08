# ADR 0002: Database Profile Strategy

- Status: Observed baseline

## Context
The repository contains H2 default configuration and separate MySQL and PostgreSQL profile settings/resources.

## Decision
Use existing Spring profiles to select database configuration. Retain H2 as the initial local baseline unless an exercise requires an external database.

## Consequences
- Persistence changes must consider all supported profiles.
- Integration tests should cover supported databases where practical.
- In-memory behaviour is not persistent deployment behaviour.
- New database technology requires a separate decision record.
