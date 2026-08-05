# Day 2 Assignment — Context and Request Budget Design

## Scenario

Design the request envelope for an employee-policy assistant. A request may include system instructions, the latest four conversation turns, an employee question, up to six retrieved chunks, and a concise answer with citations.

## Deliverables

1. a context-budget table with percentage or token allocations;
2. an explicit truncation/selection policy;
3. behavior when the question alone exceeds its allocation;
4. behavior when evidence exceeds its allocation;
5. a Java 21 `TokenBudget` or `RequestBudget` record with validation notes;
6. a sealed result hierarchy covering at least six outcomes;
7. a sequence diagram from request receipt to response validation;
8. three metrics for diagnosing budget failures.

## Analysis cases

- The most relevant policy section is in chunk 6.
- Conversation history contains a conflicting old policy.
- The provider returns a rate limit response.
- The model returns a fluent answer but no citations.
- Ten concurrent requests arrive while the provider quota allows four.

## Acceptance criteria

The design prioritizes instructions and evidence deliberately, reserves output capacity, distinguishes retryable from non-retryable failures, and does not mistake virtual threads for unlimited capacity.

