# Trainer Guide

## Recommended classroom rhythm

Use a repeatable six-hour pattern:

| Block | Duration | Method |
| --- | ---: | --- |
| Retrieval practice | 20 min | recap questions without notes |
| Concept lesson | 70 min | explanation plus diagram |
| Java translation | 60 min | annotated snippet walkthrough |
| Case analysis | 60 min | groups identify decisions and risks |
| Pattern lesson | 60 min | compare acceptable designs |
| Assignment studio | 70 min | trainer coaching, no solution broadcast |
| Quiz and reflection | 40 min | individual attempt, answer rationale |

## How to teach snippets

Ask learners to annotate each fragment with five questions:

1. What responsibility does this type or method own?
2. Which information is trusted, and which is untrusted?
3. What can fail before, during, and after the model call?
4. Which part is provider-specific?
5. How would the design be tested without calling a live model?

Do not convert the fragments into a trainer-led typing demonstration. The educational value is in boundary reasoning.

## Common misconceptions to surface

| Misconception | Corrective explanation |
| --- | --- |
| An LLM is a database | It generates token sequences; it does not guarantee exact stored facts. |
| Low temperature guarantees truth | Sampling settings influence variation, not factual correctness. |
| RAG trains the model | RAG adds retrieved context at inference time; it does not update model weights. |
| A longer prompt is always better | Irrelevant context can increase cost and distract the model. |
| JSON mode replaces validation | Syntax validity does not guarantee semantic or business validity. |
| An SDK removes provider concerns | It reduces protocol boilerplate, but quotas, capabilities, data policy, and errors remain. |
| An agent should decide everything | High-impact actions need bounded tools, policy checks, and often human approval. |

## Whiteboard prompts

- Draw where probabilistic behavior enters an otherwise deterministic Java request path.
- Mark trust boundaries in a RAG pipeline.
- Separate “model instruction,” “business rule,” and “authorization policy.”
- Show how a provider outage propagates to an HTTP client.
- Locate the point at which retrieved text becomes prompt input.

## Feedback model

Use **claim → evidence → consequence → improvement**:

- Claim: “The design is not grounded.”
- Evidence: “The answer path sends no retrieved sources.”
- Consequence: “Policy questions may be answered from model memory.”
- Improvement: “Retrieve approved documents, pass bounded excerpts, and require citation IDs.”

## Handling changing versions

Keep the conceptual lesson stable and update only the version matrix and API excerpts. Do not redesign the curriculum around every SDK release. Re-run adapter contract and evaluation checks after dependency changes.

## Academic integrity

Assignments intentionally require diagrams, trade-off notes, failure cases, and oral defense. A syntactically impressive answer without decision rationale should not receive full credit.
