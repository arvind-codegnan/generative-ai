# Day 6 Interview Questions and Answers

1. **What is an embedding?**  
   A numeric vector representing features of content so semantic relationships can be compared.

2. **What does cosine similarity tell you?**  
   How aligned two vectors are under the embedding representation; it does not prove relevance or truth.

3. **Why chunk documents?**  
   Retrieval and context windows need bounded, focused units rather than entire documents.

4. **Why store metadata with a vector?**  
   For filtering, authorization, source citation, lifecycle, deletion, freshness, and debugging.

5. **What is hybrid search?**  
   Combining semantic/vector and lexical/keyword retrieval, often followed by merging or re-ranking.

6. **Why is overlap used?**  
   To retain context across chunk boundaries, at the cost of duplication and extra tokens/storage.

7. **Can vectors from two embedding models be mixed?**  
   Generally no; dimensions and representation spaces may differ. Use versioned indexes and migration.

8. **Where should access filters apply?**  
   Before or within retrieval, so unauthorized text never reaches the model.

9. **What is recall@k?**  
   The proportion of relevant items retrieved in the top k results.

10. **Why not set top-k very high?**  
    Extra context costs tokens and may introduce irrelevant/conflicting evidence that harms generation.

