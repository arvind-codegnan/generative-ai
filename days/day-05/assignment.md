# Day 5 Assignment — Core Java GenAI Application Blueprint

## Scenario

Design a non-Spring Java 21 employee-onboarding assistant. It may use Java `HttpClient` or the official OpenAI SDK behind an adapter. Do not create a runnable project.

## Deliverables

- package tree for boundary, application, domain, infrastructure and bootstrap;
- component diagram;
- command, output DTO and sealed result fragments;
- `TextGenerator` and `EvidenceRetriever` ports;
- official-SDK and direct-HTTP adapter skeletons;
- composition-root fragment showing one selected adapter;
- validated configuration and secret-provider design;
- result mapping for CLI, batch or conceptual HTTP boundary;
- decorator order for metrics, rate limiting and retry;
- unit, boundary, adapter-contract and evaluation test strategy;
- one ADR comparing a single module with conceptual Maven modules.

## Design defects to avoid

- `main` method or runnable server;
- Spring/Jakarta framework imports or annotations;
- provider DTO in application/domain packages;
- service locator or mutable global client;
- prompt concatenation at the external boundary;
- raw generated string accepted without validation;
- API key in a record, source file or Maven configuration;
- multiple hidden retry owners.

## Acceptance criteria

Every dependency is visible in constructors, object construction is understandable without a container, provider types remain isolated, expected outcomes are explicit, and application tests require no network access.

