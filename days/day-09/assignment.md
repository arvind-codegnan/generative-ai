# Day 9 Assignment — Evaluation and Operations Plan

## Scenario

Prepare a release gate for the Day 7 travel-policy RAG assistant.

## Deliverables

- threat model with at least eight threats;
- 25-case evaluation dataset design across normal, edge, adversarial, safety, and no-evidence cases;
- deterministic checks and human/model-judge rubrics;
- retrieval, generation, safety, latency, cost, and reliability metrics;
- explicit pass/fail thresholds and critical gates;
- Java record sketches for evaluation case, score, observation, and release gate;
- dashboard layout in table form;
- three alert definitions with investigation steps;
- privacy-aware logging policy;
- rollback and incident-response decision tree.

## Acceptance criteria

Every metric serves a decision, critical harms cannot be hidden by averages, retrieval is measured separately, and operational telemetry avoids unnecessary sensitive content.

