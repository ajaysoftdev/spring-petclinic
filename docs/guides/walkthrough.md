# Source Walkthrough

## 1. Startup
Start at PetClinicApplication.java in the root package. Inspect application annotations and runtime hints before changing startup behaviour.

## 2. Domain
Read shared classes in model/, then Owner, Pet, PetType and Visit in owner/. Read Vet and Specialty in vet/. Compare entity relationships with SQL schema.

## 3. Web layer
Inspect OwnerController, PetController, VisitController, VetController and WelcomeController. Trace route mapping, binding, validation, repository call and returned view. Then inspect the matching Thymeleaf template.

## 4. Persistence
Read OwnerRepository and VetRepository, then database schema and seed data under src/main/resources/db. Confirm query and database portability.

## 5. Configuration
Inspect CacheConfiguration, WebConfiguration, application.properties and database profiles. Confirm Actuator settings from effective configuration.

## 6. Tests
Start with focused model/controller tests, then service/system and database integration classes. Record actual command and result.

## 7. First exercise
Choose a small, confirmed behaviour gap in the owner/pet/visit flow. Write a ticket, add a failing regression test, implement the smallest fix and verify relevant tests. Do not invent a defect.
