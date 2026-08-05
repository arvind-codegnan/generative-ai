# Day 5 Interview Questions and Answers

1. **What is a composition root?**  
   The single place that creates concrete objects and connects them through application-owned interfaces.

2. **Why should application code not import provider SDK types?**  
   It prevents vendor coupling from spreading and allows deterministic fakes or another adapter.

3. **What is the difference between a port and an adapter?**  
   A port is an application-required capability; an adapter translates a concrete technology into that capability.

4. **Why avoid a service locator?**  
   It hides dependencies, creates runtime lookup failures, and makes tests and reasoning harder.

5. **Where should configuration be validated?**  
   At startup/bootstrap, before constructing clients and accepting work.

6. **What belongs in a boundary mapper?**  
   Translation between external DTO/protocol shapes and application commands/results—not prompts or provider logic.

7. **Why use typed application results instead of only exceptions?**  
   Expected outcomes such as no evidence or policy rejection need explicit protocol-independent handling.

8. **What is a decorator useful for?**  
   Adding cross-cutting behavior such as metrics, rate limiting, or retry around an interface without changing the use case.

9. **Does a virtual-thread executor provide backpressure?**  
   No. Concurrency and downstream quotas must still be bounded explicitly.

10. **How is an application service tested without a model call?**  
    Inject deterministic fake implementations of its ports and verify its orchestration and result decisions.

