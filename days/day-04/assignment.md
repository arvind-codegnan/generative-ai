# Day 4 Assignment — Provider Adapter Design

## Scenario

Design a Core Java adapter for a support-response draft use case. The application may later switch between an official OpenAI SDK and another provider.

## Deliverables

- provider-neutral `GenerationRequest` and sealed `GenerationResult`;
- `TextGenerator` port;
- class diagram showing SDK adapter, mappers, configuration, retry policy, and metrics;
- error-mapping table for 400, 401/403, 408, 429, 5xx, malformed response, and content refusal;
- 2-second deadline allocation;
- secret-loading explanation;
- six deterministic unit-test scenarios using a stub;
- decision record comparing raw HTTP and the official SDK.

## Constraints

No runnable client, hard-coded endpoint, actual key, full JSON serializer, or real API invocation. Snippets must show responsibilities without completing provider wiring.

## Acceptance criteria

Provider types remain isolated, retries are bounded and classified, raw output is validated, and operational identifiers survive mapping without leaking sensitive content.
