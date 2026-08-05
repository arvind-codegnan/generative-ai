# Capstone Rubric

Total: 100 points.

| Criterion | Points | Full-credit evidence |
| --- | ---: | --- |
| Problem and boundaries | 8 | bounded user task, non-goals, harm and escalation |
| Architecture/data flow | 12 | readable components, trust boundaries, failure paths |
| Java 21 design | 10 | useful records/sealed results/ports, validation awareness |
| Maven and versions | 6 | release 21, parent/BOM roles, dated compatibility rationale |
| Core Java architecture | 10 | explicit composition, clean layers, adapter containment, configuration/security |
| Prompt/output contract | 10 | explicit task/context/constraints/fallback/schema |
| Retrieval/grounding | 10 | justified RAG choice, source/access/citation lifecycle |
| Tools/workflow | 8 | least privilege, validation, approval, idempotency/budgets |
| Safety/privacy | 8 | threat model and defense in depth |
| Evaluation/release gate | 10 | representative cases, metrics, thresholds, critical gates |
| Reliability/observability/cost | 5 | deadlines, retries, degradation, telemetry and budgets |
| Communication/defense | 3 | concise presentation and ownership of trade-offs |

## Critical deductions

Any item can cap the result below 60% until corrected:

- secrets in source/config examples;
- model alone enforces authorization;
- cross-tenant retrieval is possible;
- generated arguments execute side effects without validation/approval;
- no safe no-evidence or provider-failure path;
- quality asserted without an evaluation plan.

## Viva prompts

1. Which component would you replace to change providers?
2. Demonstrate how an unauthorized chunk is prevented from reaching the model.
3. Which failure is most harmful, and which release gate catches it?
4. What happens after a timeout if a tool may already have succeeded?
5. Which assumption would trigger architecture review?
