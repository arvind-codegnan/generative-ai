# Day 3 Interview Questions and Answers

1. **What are the main parts of a production prompt?**  
   Scope/role, task, trusted context, constraints, output contract, and fallback behavior.

2. **Why separate instructions from data?**  
   User and retrieved content may contain conflicting or malicious instructions. Their role must be explicit.

3. **What is zero-shot prompting?**  
   Asking the model to perform a task from instructions without demonstrations.

4. **When is few-shot prompting useful?**  
   When examples clarify nuanced labels, boundaries, tone, or format better than instructions alone.

5. **Does structured output eliminate hallucination?**  
   No. It constrains shape, not truth, grounding, or business validity.

6. **Why use an enum for response status?**  
   It defines a closed set of application outcomes that Java can validate and handle explicitly.

7. **What is prompt injection?**  
   Untrusted input attempts to override application instructions or cause unintended disclosure/action.

8. **Why version prompts?**  
   Prompt changes alter behavior; versions support evaluation, diagnosis, audit, rollback, and comparison.

9. **Should authorization rules be in the system prompt?**  
   They may be described for behavior, but enforcement must remain in trusted deterministic code.

10. **How do you know one prompt is better?**  
    Compare it on a fixed representative evaluation set using explicit task, safety, format, latency, and cost criteria.

