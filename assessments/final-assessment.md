# Final Assessment

Time: 120 minutes. Total: 100 marks.

## Section A — Concepts (20 marks)

Answer any five; 4 marks each.

1. Explain why low temperature does not guarantee factual output.
2. Distinguish prompt engineering, RAG, and fine-tuning.
3. Explain context budgeting with a practical Java application example.
4. Compare semantic and lexical retrieval.
5. Explain structured output and the validation still required.
6. Distinguish tool calling, workflow, and agent.

## Section B — Core Java design (25 marks)

1. Design a sealed result hierarchy for generated, no-evidence, policy-rejected, unavailable, and invalid-output outcomes. Explain HTTP mapping. (10)
2. Draw a Core Java layered component diagram with an explicit composition root that hides provider types behind a port. (8)
3. Explain how Java 21 virtual threads may help and which controls remain mandatory. (7)

## Section C — RAG case (20 marks)

A passport-document assistant answers from country-specific government checklists. Design:

- chunk metadata and access/effective-date filters;
- ingestion/query flow;
- no-evidence and conflicting-evidence behavior;
- citation validation;
- three retrieval and three generation metrics.

## Section D — Safety and operations (20 marks)

Threat-model a support assistant that can read tickets and propose closure. Cover injection, cross-tenant data, secrets, output handling, approval, idempotency, budgets, audit, kill switch, and incident behavior.

## Section E — Decision defense (15 marks)

Write an ADR comparing direct Java `HttpClient` and the official OpenAI Java SDK for a Core Java service. Include context, decision, alternatives, consequences, and review triggers. State how Maven versions are governed.

## Scoring focus

Reward explicit responsibility boundaries, typed failure, evidence/access control, measurable evaluation, operational realism, and defensible trade-offs. Syntax is secondary to correct design.
