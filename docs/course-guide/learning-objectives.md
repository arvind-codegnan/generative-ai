# Learning Objectives Matrix

Bloom levels: **R** remember, **U** understand, **A** apply, **An** analyze, **E** evaluate, **C** create.

| Day | R/U | Apply | Analyze/Evaluate | Create |
| --- | --- | --- | --- | --- |
| 1 | define GenAI vocabulary | classify use cases | identify unsuitable use cases | use-case canvas |
| 2 | explain tokens and embeddings | estimate context usage | compare sampling choices | request envelope |
| 3 | name prompt elements | write constrained prompts | diagnose prompt defects | prompt specification |
| 4 | describe API/SDK roles | map DTOs and errors | compare integration options | provider adapter |
| 5 | explain composition and ports | place objects in layers | detect SDK leakage | application blueprint |
| 6 | explain vector similarity | choose metadata filters | compare chunking strategies | search design |
| 7 | explain RAG | trace ingestion/query flow | diagnose poor grounding | RAG architecture |
| 8 | distinguish tool and agent | define tool schemas | evaluate autonomy risk | bounded workflow |
| 9 | define quality/safety metrics | score test cases | analyze failures and trade-offs | evaluation plan |
| 10 | synthesize all concepts | defend choices | review another design | capstone package |

## Java 21 mapping

| Feature | Curriculum use | Teaching caution |
| --- | --- | --- |
| Records | immutable request, result, chunk, citation and metric shapes | a record is not automatic validation |
| Sealed interfaces | closed result/failure hierarchies | avoid complexity when a simple enum suffices |
| Pattern matching for `switch` | explicit handling of result variants | all variants still require domain decisions |
| Text blocks | readable prompt fragments and JSON examples | indentation and interpolation still need care |
| Virtual threads | conceptual concurrency for blocking I/O | concurrency does not remove rate limits or backpressure |
