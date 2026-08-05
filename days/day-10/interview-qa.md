# Day 10 Interview Questions and Answers

1. **What is the most important boundary in a GenAI service?**  
   The boundary that treats model input/output as controlled but untrusted data while deterministic application code retains policy and side effects.

2. **Should a GenAI application start as microservices?**  
   Not automatically. A modular Core Java application is often simpler; distribute only for justified scale, ownership, isolation, or deployment needs.

3. **Why use a model capability profile?**  
   It expresses application requirements without hard-coding provider/model identity throughout business code.

4. **What is graceful degradation for RAG?**  
   Provide a transparent safe alternative, such as source search, rather than unsupported generation when retrieval fails.

5. **What belongs in an ADR?**  
   Context, decision, alternatives, consequences, and conditions that trigger review.

6. **How do Maven and an official SDK reduce different risks?**  
   Maven supports reproducible build/dependency management; an SDK reduces provider protocol boilerplate. Neither guarantees model quality.

7. **How would you switch providers?**  
   Implement the existing capability port, map errors/metadata, verify data policy/features, and pass the full evaluation/release gate before cutover.

8. **What should a production rollback restore?**  
   A known combination of application, prompt, model profile, index/retrieval, tool, and policy configuration.

9. **How do you answer a GenAI system-design interview question?**  
   Clarify requirements, separate deterministic/model work, show boundaries/data flow, define failure and controls, then evaluate trade-offs.

10. **What demonstrates real understanding beyond a demo?**  
    Explicit contracts, safe failure, source/access governance, evaluation evidence, operations, and defensible design choices.
