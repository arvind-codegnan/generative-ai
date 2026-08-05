# Version Policy

## Curriculum baseline

| Component | Reference baseline | Purpose |
| --- | --- | --- |
| Java | 21 | records, sealed types, pattern matching, text blocks, HTTP client, virtual threads |
| Maven | 3.9.x conceptual baseline | lifecycle, dependency and plugin management |
| Maven Compiler Plugin | 3.15.0 | explicit Java `release` example |
| OpenAI Java SDK | 4.50.0 at verification time | optional concrete Core Java provider adapter |

The baseline was checked against primary documentation on 2026-08-05. These coordinates are learning references, not a claim that copied fragments form an executable application.

## Non-Spring rule

This repository must not add Spring Boot, Spring AI, Spring Framework, Jakarta application frameworks, DI containers, starters, annotations, or framework-specific configuration. Core Java object composition is part of the learning objective.

## Update rules

1. Keep `<maven.compiler.release>21</maven.compiler.release>` explicit.
2. Prefer a stable SDK release and record the verification date.
3. Keep provider SDK types inside a dedicated adapter package.
4. Configure model capability/profile at the application boundary; do not scatter model IDs through domain code.
5. Re-check authentication, request/response mapping, error taxonomy, streaming, structured output, tool calling, and retry behavior after SDK upgrades.
6. Re-run the semantic evaluation set before accepting any provider, model, prompt, or retrieval change.
7. Keep direct HTTP as a documented alternative even when an SDK is selected.

## Trainer compatibility questions

- Does the SDK support Java 21 and the provider feature being taught?
- Which API surface does the SDK use for generation?
- Are request parameters supported by the chosen model/capability?
- Does the client implement hidden retries, and who owns the total deadline?
- Can request IDs, usage, raw status and relevant headers be retained for diagnosis?
- How are structured-output and tool-call variants represented?

