# High-Level Design: Spring PetClinic

- Status: Observed from repository source; runtime verification pending
- Upstream project: https://github.com/spring-projects/spring-petclinic

## 1. Purpose
Describe the current application for onboarding, impact analysis and engineering exercises.

## 2. Product scope
Spring PetClinic is a sample veterinary clinic management application. Its domain includes owners, pets, pet types, visits, veterinarians and specialties. The repository presents a server-rendered web application using Spring MVC and Thymeleaf.

## 3. Context view

    Clinic user -> Browser -> Spring MVC application
                                  |
                           Domain / validation
                                  |
                           Spring Data JPA
                                  |
                       H2 / MySQL / PostgreSQL

The active profile determines the database configuration.

## 4. Technology and build
Observed in the current repository:
- Maven property java.version is 17.
- Spring Boot parent and dependency versions are declared in pom.xml.
- Maven and Gradle wrapper scripts are present.
- Spring MVC, Thymeleaf, validation, Spring Data JPA and Actuator dependencies are declared.
- H2, MySQL and PostgreSQL drivers are included.
- Caffeine and Spring cache dependencies are present.
- Test dependencies include web, validation, JPA and Testcontainers support.

Consult current build files for exact version numbers.

## 5. Logical modules

| Package | Responsibility |
|---|---|
| model | Shared entity base classes and person model |
| owner | Owners, pets, pet types, visits, repositories, controllers and validation |
| vet | Veterinarians, specialties, repository and controller |
| system | Welcome/system web configuration, cache configuration and crash endpoint |
| root | Application entry point and runtime hints |

## 6. Main user journeys
Search owners; view owner and pet details; create/update owners and pets; record pet visits; view veterinarians and specialties. Exact routes, validation and templates must be confirmed from source.

## 7. Persistence
JPA entities and Spring Data repositories provide persistence. H2 schema/seed data are under src/main/resources/db/h2; separate MySQL and PostgreSQL profiles and SQL resources are present.

## 8. Cross-cutting concerns
Bean validation, JPA persistence, cache configuration, Actuator dependency, profile-specific configuration and GitHub Actions build workflows. Exact exposed management endpoints and cache behaviour require verification.

## 9. Deployment
The repository includes Docker Compose for database services and a cluster deployment/testing workflow. This does not prove a cluster is currently deployed.

## 10. Open questions
Confirm active profiles, actuator exposure, cache regions/eviction, supported deployment targets, operational metrics and alert thresholds.

## 11. Related
[LLD](LLD.md) · [Data model](data-model.md) · [Security](security.md) · [Threat model](threat-model.md)
