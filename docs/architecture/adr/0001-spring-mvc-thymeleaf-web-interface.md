# ADR 0001: Spring MVC and Thymeleaf Interface

- Status: Observed baseline

## Context
The current build declares Spring MVC and Thymeleaf dependencies. The application uses server-rendered pages and form workflows.

## Decision
Document the existing MVC/Thymeleaf architecture as the baseline. This records an observed characteristic, not a new technology selection.

## Consequences
- UI changes commonly involve controllers, binding, validation and templates.
- Server-side validation and safe rendering matter.
- A separate REST API must not be assumed.
- Any future interface redesign requires an ADR and migration analysis.
