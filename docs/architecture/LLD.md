# Low-Level Design: Spring PetClinic

- Status: Source-informed; runtime verification pending
- Parent: [HLD](HLD.md)

## 1. Entry point
The application entry point is PetClinicApplication.java in the root package org.springframework.samples.petclinic.

## 2. Package map

    org.springframework.samples.petclinic
    ├── PetClinicApplication
    ├── PetClinicRuntimeHints
    ├── model: BaseEntity, NamedEntity, Person
    ├── owner: Owner, OwnerController, OwnerRepository,
    │         Pet, PetController, PetType, PetTypeRepository,
    │         PetTypeFormatter, PetValidator, Visit, VisitController
    ├── vet: Vet, Specialty, Vets, VetController, VetRepository
    └── system: CacheConfiguration, WebConfiguration,
                WelcomeController, CrashController

This is a partial package map from current directory inspection. Inspect the full tree before asserting no other classes exist.

## 3. Request processing
The application uses Spring MVC. A typical form interaction binds request fields to model objects, invokes validation and repository operations, then renders a Thymeleaf view. Confirm each route and exact call path in controller and template source.

## 4. Persistence boundary
Owner and Vet repositories are in their domain packages. JPA entities represent persistent objects. Keep data access in repository abstractions rather than view templates.

## 5. Validation
The owner package contains PetValidator and the build declares Spring validation dependencies. Verify controller binding and validator invocation together.

## 6. System configuration
The system package contains CacheConfiguration and WebConfiguration. Review their actual cache manager, web resource and formatting configuration before changing behaviour.

## 7. Database
application.properties, application-mysql.properties and application-postgres.properties select configuration. SQL resources exist for H2, MySQL and PostgreSQL.

## 8. Tests
The test tree includes model, owner, service, system and vet packages, plus database/application integration test classes. Inspect test methods before making coverage claims.

## 9. Change impact checklist
For owner/pet/visit changes, review controller binding, domain relationship, validation, repository behaviour, Thymeleaf forms, regression tests and database-profile compatibility.

## 10. Limitations
This is a package-level source map, not a complete call graph. Method-level sequence diagrams and a full route inventory require further source inspection.
