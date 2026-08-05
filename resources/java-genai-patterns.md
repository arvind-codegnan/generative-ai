# Java 21 Patterns for GenAI Systems

## 1. Immutable request contract

```java
// Concept fragment
record GenerationRequest(
        String useCase,
        String userInput,
        Map<String, String> trustedContext,
        OutputContract outputContract,
        RequestPolicy policy) {
}
```

Records reduce accidental mutation, but a compact constructor or factory is still needed to enforce null, length, and allow-list constraints.

## 2. Provider-neutral port

```java
// Boundary sketch
interface TextGenerator {
    GenerationResult generate(GenerationRequest request);
}
```

The domain/application layer depends on a capability, not a vendor DTO. Provider-specific token usage, request IDs, and finish reasons can be translated into neutral metadata without discarding observability.

## 3. Explicit result algebra

```java
// Concept fragment
sealed interface GenerationResult
        permits Generated, Rejected, Unavailable, InvalidOutput { }

record Generated(String text, List<Citation> citations, Usage usage)
        implements GenerationResult { }
record Rejected(String policyCode) implements GenerationResult { }
record Unavailable(boolean retryable, String category) implements GenerationResult { }
record InvalidOutput(List<String> violations) implements GenerationResult { }
```

This is more expressive than returning `null`, an empty string, or a provider exception from every failure path.

## 4. Exhaustive handling

```java
// Concept fragment
return switch (result) {
    case Generated g -> mapSuccess(g);
    case Rejected r -> mapPolicyResponse(r);
    case Unavailable u -> mapAvailabilityResponse(u);
    case InvalidOutput i -> mapValidationResponse(i);
};
```

Pattern matching encourages explicit outcomes. The HTTP status mapping remains a business/API design decision.

## 5. Separate prompt assembly

```java
// Boundary sketch
interface PromptAssembler {
    PromptEnvelope assemble(UseCaseInput input, List<GroundingChunk> evidence);
}
```

A controller should not concatenate system instructions, user input, and retrieved documents. Central assembly supports versioning, injection defenses, token budgets, and testing.

## 6. Output validation pipeline

```java
// Concept fragment
ValidatedAnswer validate(ModelOutput output) {
    var syntax = schemaValidator.check(output.rawText());
    var semantics = businessValidator.check(syntax.parsedValue());
    var grounding = citationValidator.check(semantics.value());
    return policyValidator.check(grounding.value());
}
```

The order is illustrative. Each stage should return failures as data when they are expected outcomes.

## 7. Decorator for cross-cutting controls

```java
// Boundary sketch
final class MeteredTextGenerator implements TextGenerator {
    private final TextGenerator delegate;
    private final GenerationMetrics metrics;

    public GenerationResult generate(GenerationRequest request) {
        // start timer; delegate; record category and usage; never log secrets
        throw new UnsupportedOperationException("reference fragment");
    }
}
```

The deliberate exception prevents this from masquerading as a working implementation.

## 8. Bounded concurrency with virtual threads

```java
// Concept fragment
try (var executor = Executors.newVirtualThreadPerTaskExecutor()) {
    // Submit independent blocking calls only after applying a concurrency limit.
    // Collect results with a deadline; cancel work that no longer has a caller.
}
```

Virtual threads reduce the cost of blocked platform threads. They do not increase provider quotas, eliminate timeouts, or provide backpressure. Pair them with a semaphore/bulkhead and request budget.

## 9. Provider adapter

```java
// Boundary sketch
final class OpenAiTextGenerator implements TextGenerator {
    private final ProviderClient client;
    private final ProviderRequestMapper requestMapper;
    private final ProviderResponseMapper responseMapper;
    private final RetryPolicy retryPolicy;
}
```

Keep provider types inside this adapter. A direct `HttpClient` adapter and an official-SDK adapter may implement the same `TextGenerator` port, but only one should own a deployed capability.

## 10. Human approval as a state

```java
// Concept fragment
sealed interface ActionState permits Proposed, Approved, Rejected, Executed, Failed { }
```

Human approval should be persisted and auditable. A boolean such as `approved=true` inside model-provided JSON is not approval.
