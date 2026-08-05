# Evaluation Checklist

## Start with a testable claim

Bad: “The assistant is accurate.”

Better: “On the approved 100-question HR policy set, at least 92% of answers are fully supported by retrieved policy passages, no answer cites a nonexistent source, and unsafe requests are refused in all critical cases.”

## Dataset design

- [ ] representative normal cases;
- [ ] rare but important edge cases;
- [ ] ambiguous and insufficient-evidence cases;
- [ ] adversarial/prompt-injection cases;
- [ ] sensitive-data cases;
- [ ] expected citations or scoring rubric;
- [ ] severity label for failures;
- [ ] dataset version and change notes;
- [ ] no contamination with private production data.

## Metrics

| Dimension | Example measure |
| --- | --- |
| Task correctness | rubric score or exact/semantic match where appropriate |
| Groundedness | claims supported by supplied evidence |
| Citation quality | source exists and entails the claim |
| Retrieval | recall@k, precision@k, mean reciprocal rank |
| Safety | critical violation count, refusal precision/recall |
| Format | schema-valid response rate |
| Latency | p50, p95, p99 end-to-end and model duration |
| Cost | input/output tokens and currency per successful task |
| Reliability | success, timeout, retry and provider-error rates |

## Comparison discipline

When comparing prompt, model, chunking, or retrieval changes:

1. freeze the evaluation set;
2. change one major variable at a time;
3. record configuration and prompt version;
4. compare both aggregate and critical-case results;
5. inspect failures, not only the average score;
6. require a rollback criterion.

## LLM-as-judge caution

A model-based judge can scale rubric scoring, but it introduces its own bias and variability. Calibrate it against human-scored examples, blind the candidate identity/order where possible, use explicit rubrics, and retain human review for high-impact conclusions.

