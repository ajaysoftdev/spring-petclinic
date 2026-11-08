# Local Quickstart

## 1. Prerequisites
JDK 17 or newer, Git and a terminal. Maven and Gradle wrapper scripts are included, so global build-tool installation is not initially required.

## 2. Clone

    git clone https://github.com/ajaysoftdev/spring-petclinic.git
    cd spring-petclinic

## 3. Verify Java and Maven Wrapper

Windows PowerShell:
    java -version
    .\mvnw.cmd -version

macOS/Linux:
    java -version
    ./mvnw -version

The Maven build currently declares Java 17. If Java is missing, install a JDK 17 distribution, reopen the terminal and repeat the checks.

## 4. Run tests

    ./mvnw test

Windows:
    .\mvnw.cmd test

Record actual exit status and output. This document does not claim tests have already been run.

## 5. Start

    ./mvnw spring-boot:run

Windows:
    .\mvnw.cmd spring-boot:run

Open http://localhost:8080. Upstream documentation describes H2 as the default local database.

## 6. Database profiles
MySQL and PostgreSQL profiles and setup resources are available. Read the profile properties and database scripts before activating them.

## 7. Baseline
Record JDK, wrapper version, commit, test command, result and environment blockers.
