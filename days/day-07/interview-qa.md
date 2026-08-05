# Day 7 Interview Questions and Answers

1. **What problem does RAG solve?**  
   It supplies external, current, private, or citable evidence to a model at inference time.

2. **Does RAG guarantee correct answers?**  
   No. Retrieval, source quality, context sufficiency, generation, and citation can all fail.

3. **What are the two main RAG pipelines?**  
   Offline/nearline ingestion and online query/answering.

4. **Why preserve the original query?**  
   Transformations can alter intent; the original is needed for evaluation, audit, and fallback.

5. **What is re-ranking?**  
   Reordering retrieved candidates using a method optimized for relevance after initial retrieval.

6. **What is groundedness?**  
   The degree to which answer claims are supported by the supplied authoritative evidence.

7. **Why validate citation IDs server-side?**  
   Models can invent identifiers; only IDs retrieved for that request are legitimate candidates.

8. **What should happen when no evidence is found?**  
   Return an explicit insufficient-evidence/no-evidence outcome or escalate, rather than answer from unsupported memory.

9. **Can retrieval filters be left to the prompt?**  
   No. Authorization and tenant isolation must be applied before evidence reaches the model.

10. **How do you improve RAG systematically?**  
    Evaluate each stage, inspect failures, then tune sources, parsing, chunks, retrieval, ranking, assembly, or prompts based on evidence.

