# Course Syllabus

## Course title

Generative AI Application Design with Java 21, Maven, Core Java, Java HTTP, and OpenAI

## Duration and mode

- Duration: 10 working days
- Contact time: 60 hours
- Suggested batch size: 20–30 learners
- Mode: instructor-led theory, whiteboarding, snippet analysis, design exercises, quizzes, and capstone reviews

## Prerequisites

Learners should be able to:

- create Java classes, records, interfaces, collections, and exceptions;
- explain inheritance, composition, immutability, and dependency inversion;
- read a Maven `pom.xml` and name the `compile`, `test`, and `package` phases;
- understand REST vocabulary, HTTP status classes, JSON objects, and environment variables;
- describe interfaces, composition, DTO mapping, HTTP, JSON, configuration, exceptions, and concurrency.

The course does not require prior machine-learning mathematics, Python, data science, or cloud deployment.

## Course-level outcomes

By the end of Day 10, a learner can:

1. distinguish generative models from traditional deterministic software and predictive ML;
2. explain tokens, context windows, embeddings, attention, inference, and sampling at an application-developer level;
3. design prompts with explicit roles, context, constraints, examples, and output contracts;
4. model GenAI requests and responses using Java 21 types and clean boundaries;
5. compare direct Java HTTP and an official Java SDK integration;
6. design Core Java layers without leaking provider DTOs into domain code;
7. explain semantic search and create a defensible RAG ingestion/query design;
8. define safe tool contracts and bounded agentic workflows;
9. plan offline/online evaluation, security controls, observability, latency, and cost management;
10. present and defend a production-oriented Java GenAI architecture.

## Detailed timetable

| Day | Morning session | Afternoon session | Assessment |
| --- | --- | --- | --- |
| 1 | AI/ML/GenAI taxonomy; model lifecycle | Java 21 and Maven mapping; use-case selection | Diagnostic + use-case pitch |
| 2 | Tokens, embeddings, transformers, inference | Context and sampling; concurrency discussion | Mechanics quiz |
| 3 | Prompt anatomy and patterns | Structured outputs and prompt lifecycle | Prompt critique |
| 4 | REST/SDK integration boundaries | errors, retry, timeout, secrets, provider adapters | Adapter design review |
| 5 | Core Java layering and configuration | composition root, service/port/adapter, output mapping | application blueprint review |
| 6 | Embedding spaces and similarity | chunking, metadata, vector-store abstraction | Search design quiz |
| 7 | RAG ingestion/query pipelines | retrieval quality, grounding, citations, failure modes | RAG design review |
| 8 | tool calling and workflow control | agents, state, idempotency, human approval | Threat-model review |
| 9 | safety and responsible AI | evaluation, observability, cost/latency | Evaluation plan review |
| 10 | capstone architecture clinic | presentation, viva, interview preparation | Final assessment |

## Delivery principles

### Core Java before libraries

The course expresses each concern as a Java interface, record, sealed result, object collaboration, or data flow. SDK and HTTP details stay in adapters so library syntax never replaces understanding.

### Contracts before prompts

A prompt is treated as part of a larger contract: input policy, context, expected schema, validation, error handling, monitoring, and human accountability.

### Evaluation before optimization

No prompt, model, retriever, or agent design is considered “better” without an agreed dataset and measurable acceptance criteria.

### Reference fragments, not applications

The repository contains just enough syntax to discuss a pattern. Imports, surrounding classes, dependencies, infrastructure, and operational configuration may be deliberately absent.

## Capstone choices

Learner teams select one domain:

- HR policy assistant with citation-backed answers;
- employee onboarding guide;
- internal Java code-review assistant;
- customer-support response draft service;
- passport-document checklist assistant;
- course-content question generator with faculty review.

Each team submits a use-case canvas, architecture, data-flow diagram, prompt contract, RAG/tool decision, safety controls, evaluation plan, Maven dependency rationale, Core Java package sketch, and operational runbook excerpt.
