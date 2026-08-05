# Day 10 Assignment — Capstone Architecture Package

## Choose one domain

- HR policy assistant;
- passport-document checklist assistant;
- Java code-review assistant;
- customer-support draft assistant;
- course-content question generator.

## Required package

1. problem statement, users, value, non-goals, and harm analysis;
2. system context diagram and end-to-end sequence;
3. Maven dependency/version rationale;
4. Java 21 package design, records, sealed results, and capability ports;
5. Core Java package, composition-root and component blueprint;
6. prompt specification and output schema;
7. RAG design or written justification for not using RAG;
8. tool workflow or written justification for no tools;
9. threat model, privacy controls, and human oversight;
10. evaluation dataset outline, metrics, thresholds, and release gate;
11. timeout, retry, concurrency, cost, and degradation strategy;
12. three ADRs and one rollback plan;
13. ten-minute presentation and five-minute viva.

## Prohibited shortcuts

- runnable generated application as a substitute for design;
- credentials or live personal data;
- “the model handles it” without application control;
- architecture without failure states;
- quality claims without evaluation evidence.

## Acceptance criteria

The package is internally consistent, provider coupling is bounded, access is enforced before evidence/tool execution, expected failures are typed, and release is governed by measurable quality and safety gates.
