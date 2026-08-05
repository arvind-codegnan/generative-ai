# Interview Question Bank Index

The course contains 100 answered questions, organized by day:

| Topic | Questions and answers |
| --- | --- |
| Foundations and Java role | [Day 1](../days/day-01/interview-qa.md) |
| Tokens, context, embeddings, inference | [Day 2](../days/day-02/interview-qa.md) |
| Prompt engineering and structured output | [Day 3](../days/day-03/interview-qa.md) |
| Core Java, HTTP, SDKs, resilience | [Day 4](../days/day-04/interview-qa.md) |
| Core Java application architecture | [Day 5](../days/day-05/interview-qa.md) |
| Semantic search and chunking | [Day 6](../days/day-06/interview-qa.md) |
| RAG and citations | [Day 7](../days/day-07/interview-qa.md) |
| Tools and agents | [Day 8](../days/day-08/interview-qa.md) |
| Safety, evaluation, and operations | [Day 9](../days/day-09/interview-qa.md) |
| Production architecture | [Day 10](../days/day-10/interview-qa.md) |

## Fifteen system-design prompts

Use these for mock interviews; answer with requirements, boundary/data-flow, failure states, controls, evaluation, and trade-offs.

1. Design an HR policy assistant with citations.
2. Design a Java code-review assistant that cannot merge code.
3. Design a customer-support drafting API with human approval.
4. Design semantic search over versioned product manuals.
5. Design a multi-tenant RAG service.
6. Migrate a direct `HttpClient` integration to an official SDK without changing application code.
7. Switch embedding models without downtime.
8. Add streaming to an existing validated response API.
9. Add a send-email tool safely.
10. Reduce p95 latency without lowering groundedness.
11. Reduce cost per accepted answer by 25%.
12. Respond to a prompt-injection incident in retrieved documents.
13. Evaluate two model profiles for a classification use case.
14. Design provider outage degradation.
15. Explain why a requested open-ended agent should be a workflow.

## Interview scoring lens

- 0: names technologies only;
- 1: explains happy-path components;
- 2: defines contracts and failure paths;
- 3: adds trust/access, evaluation and operations;
- 4: compares alternatives with measurable decision/review criteria.
