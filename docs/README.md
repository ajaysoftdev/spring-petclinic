# Spring PetClinic Documentation

This documentation describes the existing open-source sample application based on repository inspection. It is not a claim that the application was originally authored for this portfolio.

## Architecture
- [High-Level Design](architecture/HLD.md)
- [Low-Level Design](architecture/LLD.md)
- [Data model](architecture/data-model.md)
- [Security](architecture/security.md)
- [Threat model](architecture/threat-model.md)
- [ADRs](architecture/adr/)

## Developer guides
- [Local quickstart](guides/quickstart-local.md)
- [Configuration](guides/configuration.md)
- [Testing](guides/testing.md)
- [Operations](guides/operations.md)
- [Troubleshooting](guides/troubleshooting.md)
- [Source walkthrough](guides/walkthrough.md)

## API and interface
The current application is a server-rendered Spring MVC / Thymeleaf web application. This documentation does not invent a separate public REST API or OpenAPI contract. MVC routes and form workflows are documented as they are verified from controller mappings.

## Source of truth
Source code, build files, application properties, SQL scripts and tests are authoritative. Runtime behaviour remains to be verified locally. No local build, test suite or application startup is claimed by these documents.
