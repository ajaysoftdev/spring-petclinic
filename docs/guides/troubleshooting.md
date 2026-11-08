# Troubleshooting Guide

## Java and build

| Symptom | First checks |
|---|---|
| java not found | Install JDK 17+, reopen terminal, check PATH/JAVA_HOME |
| Wrapper fails | Check wrapper files, network and Java |
| Version rejected | Compare installed JDK with java.version in pom.xml |
| Dependency resolution fails | Check network/proxy and Maven repository |
| Formatting/Checkstyle fails | Read first reported file/rule |
| Test failure | Re-run smallest failing test and inspect first causal error |

## Application startup
Check port 8080, first startup exception, active Spring profile, database URL, service status and credentials for non-H2 profiles.

## Database
PetClinic has H2 default configuration and separate MySQL/PostgreSQL settings. Confirm profile and matching database service before changing SQL.

## Web behaviour
For a form issue inspect controller binding, validation invocation, model attributes and Thymeleaf template. Determine whether the fault is binding, validation, persistence or rendering.

## Reproducible defect
Include route/workflow, synthetic input, expected/actual result, environment, sanitised log excerpt and whether it reproduces on the unchanged starting commit.
