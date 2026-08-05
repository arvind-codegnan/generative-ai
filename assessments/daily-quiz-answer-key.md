# Daily Quiz Answer Key with Rationales

## Day 1

1. **B.** Inference uses an already trained model for new input.
2. Examples: authorization, exact calculation, transaction rule, database constraint.
3. **No.** RAG adds retrieved context at inference.
4. Any two: authentication, policy, validation, data access, output checks, monitoring, side effects.
5. Transport completion does not prove grounding, structure, safety, or business validity.

## Day 2

1. **No.** Token boundaries depend on the tokenizer.
2. Instructions, history, user input, evidence/tool data, reserved output.
3. Sampling variation, not confidence or truth.
4. The array remains mutable even when its reference is final.
5. Bounded concurrency/backpressure, rate-limit handling, timeout/deadline, cancellation.

## Day 3

1. Any four: role/scope, task, trusted context, constraints, output contract, fallback.
2. **No.** It is data and may contain injection.
3. It improves/constrains structure; it does not guarantee correctness or grounding.
4. For nuanced labels, boundaries, tone, or output examples.
5. To evaluate, audit, diagnose, compare, and roll back behavior changes.

## Day 4

1. Ports and adapters (dependency inversion).
2. **400.** Retrying the same invalid request will not correct it.
3. To keep cumulative work and retries within caller latency.
4. Several layers retry, multiplying downstream calls.
5. In the integration adapter/response mapper.

## Day 5

1. The explicit place that constructs concrete objects and connects them through interfaces.
2. To contain vendor coupling and allow deterministic fakes or replacement adapters.
3. It adds cross-cutting behavior such as metrics, retry, or rate limiting around a port.
4. It hides dependencies and moves construction errors to runtime lookups.
5. Domain/application and boundary unit tests; provider contract checks are separate.

## Day 6

1. **No.** It is a representation-specific closeness score.
2. Examples: document/chunk ID, version, section, tenant, security label, effective date.
3. Combined semantic and lexical retrieval.
4. Before or during retrieval, before model context is built.
5. Version a new index and re-embed/migrate with evaluation.

## Day 7

1. Ingestion and online query/answering.
2. Return no/insufficient evidence or escalate; do not invent.
3. Models can invent IDs or cite unsupported chunks.
4. Reorders candidates using a more precise relevance method.
5. Retrieval: recall@k; generation: groundedness (other valid pairs accepted).

## Day 8

1. Trusted application/tool code after validation and authorization.
2. Identity, tenant, permissions, and approval cannot be trusted from generated arguments.
3. Idempotency plus current-state validation and a bounded policy.
4. Success, denial, inability, deadline, budget, repeated failure/no progress.
5. **No.** It is untrusted data.

## Day 9

1. It can hide critical safety failures and poor subgroups/tail behavior.
2. Task quality, grounding, safety, reliability, latency, cost, format.
3. 95% of measured requests are at or below that duration.
4. The judge is probabilistic and biased; human-scored calibration tests validity.
5. Total relevant cost divided by outputs that pass acceptance criteria.

## Day 10

1. It separates application needs from changing provider/model identities.
2. Source search, async job, evaluated fallback, static guidance, tool disablement, transparent outage.
3. Context, decision, alternatives, consequences, review trigger.
4. Independent scale, ownership, isolation, deployment, or compliance boundary.
5. Prompt, model profile, retrieval/index, tool, policy, and configuration versions.
