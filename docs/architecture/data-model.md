# Data Model: Spring PetClinic

- Status: Conceptual source-informed view
- Schema locations: src/main/resources/db/h2 and database-specific resources

## 1. Domain concepts

| Entity | Purpose | Relationship |
|---|---|---|
| Person | Shared person attributes | Base model for person-related domain data |
| Owner | Pet owner/contact information | One owner may have multiple pets |
| Pet | Animal registered to an owner | References pet type; has visits |
| PetType | Pet classification | Referenced by pets |
| Visit | Clinical visit record | Belongs to a pet |
| Vet | Veterinarian profile | Associated with specialties |
| Specialty | Veterinary speciality | May be associated with multiple vets |

Confirm cardinality, cascade rules, join-table names and nullability against entity annotations and active SQL schema before a migration.

## 2. Conceptual relationships

    OWNER 1 --- many PET
    PET_TYPE 1 --- many PET
    PET 1 --- many VISIT
    VET many --- many SPECIALTY

## 3. Persistence considerations
Identifiers and inherited fields are defined in model classes. Owner, Pet and Visit are in the owner package; Vet and Specialty are in vet. Repositories provide persistence access. H2 schema/seed data and MySQL/PostgreSQL resources are separate.

## 4. Integrity questions
Verify owner deletion rules, whether pets require owners, visit date constraints, mandatory pet type, veterinarian-specialty mapping and consistency across database profiles.

## 5. Migration compatibility
Do not assume a migration history. Check schema scripts, seed data and integration tests for every supported database before changing the model.

## 6. Privacy
Owner names, addresses and telephone numbers may be personal data. Use synthetic records in screenshots, issues and test evidence.
