# Day 1 Interview Questions and Answers

1. **How does Generative AI differ from traditional Java logic?**  
   Java logic executes explicit instructions; Generative AI produces probable outputs from learned patterns. The latter needs validation and may vary.

2. **What is inference?**  
   Inference is using a trained model to generate or score an output for new input. Most application integrations happen here.

3. **Does RAG retrain an LLM?**  
   No. It retrieves relevant information and includes it in inference-time context; model weights remain unchanged.

4. **Why is a model unsuitable for exact arithmetic or authorization rules?**  
   Deterministic Java code is cheaper, testable, explainable, and reliable for exact rules. A model may produce plausible errors.

5. **What should Java own in a GenAI application?**  
   Authentication, authorization, validation, business rules, data access, retries, timeouts, output checks, auditing, and side effects.

6. **What is hallucination?**  
   Generated content that appears plausible but is incorrect or unsupported. It is a system design concern, not just a user mistake.

7. **What is the difference between training and prompting?**  
   Training changes model parameters using data and optimization; prompting supplies inference-time instructions and context.

8. **Why use records for request shapes?**  
   They provide concise immutable data carriers, useful for explicit contracts. They still require validation.

9. **What does Maven solve in this domain?**  
   Reproducible build structure, dependency and plugin management, compilation, tests, and packaging—not response correctness.

10. **Give one reason not to add GenAI to a feature.**  
    The task may already have an exact rule/search solution, or the impact of a wrong output may be unacceptable without review.

