# Day 9 Interview Questions and Answers

1. **Why is answer accuracy alone insufficient?**  
   A system must also meet grounding, safety, privacy, reliability, latency, cost, and format requirements.

2. **What is defense in depth?**  
   Multiple independent controls across input, retrieval, prompt, model, output, tools, UI, and operations.

3. **What is refusal precision?**  
   Of the cases the system refused, the proportion that should have been refused.

4. **Why track p95 latency?**  
   It exposes slower tail behavior that an average can hide.

5. **What is cost per accepted task?**  
   Total relevant cost divided by outputs meeting acceptance criteria, accounting for failures/retries.

6. **What belongs in a generation observation?**  
   Non-sensitive correlation, use case, versions, timing, usage, and categorized outcome.

7. **Why separate retrieval metrics?**  
   The generator cannot reliably use evidence that retrieval failed to supply; stage metrics locate the defect.

8. **What is an LLM-as-judge risk?**  
   The evaluator is itself probabilistic and biased; it needs calibration against human-scored examples.

9. **What is a critical release gate?**  
   A threshold that must pass regardless of aggregate improvement, such as zero cross-tenant leakage.

10. **Should prompts and responses be logged by default?**  
    No. Content may contain secrets or personal data; collect the minimum approved telemetry with controls.

