# Generative AI Glossary for Java Developers

| Term | Practical meaning | Java analogy or caution |
| --- | --- | --- |
| Artificial Intelligence | broad field of machines performing tasks associated with intelligence | umbrella term, not a library |
| Machine Learning | systems learn patterns from data instead of only explicit rules | training differs from calling an API |
| Generative AI | models produce new text, images, audio, code, or other content | output is data to validate, not trusted code |
| Large Language Model | model trained to predict and generate token sequences | not a `Map<String,String>` of facts |
| Token | unit processed by a language model | not identical to a Java character or word |
| Tokenization | conversion between content and tokens | affects limits and billing |
| Context window | maximum usable token budget for instructions, inputs, retrieved text, history, and output | like bounded request memory, but model-specific |
| Prompt | instructions and input given to a model | closer to a versioned request specification than a search query |
| System instruction | high-priority application guidance | not an authorization control by itself |
| Inference | using a trained model to produce output | the normal API-call stage |
| Parameter | learned numeric value inside a model | unrelated to Java method parameters |
| Temperature | sampling control for variation where supported | does not measure confidence or truth |
| Hallucination | plausible but unsupported or incorrect generation | design for detection and safe fallback |
| Embedding | numeric vector representing semantic features | usually `float[]`, but dimensions and meaning are model-specific |
| Cosine similarity | compares vector direction | higher score is not automatically a correct answer |
| Chunk | bounded document segment used for indexing/retrieval | preserve source and location metadata |
| Vector store | system that indexes vectors and metadata | not a replacement for the source of truth |
| Semantic search | retrieval by meaning rather than only exact keywords | often hybridized with lexical search |
| RAG | retrieve relevant content and add it to model input | changes context, not model weights |
| Grounding | constraining answers to trusted evidence | require citations and an “insufficient evidence” path |
| Fine-tuning | additional training to change model behavior | not the default fix for missing current knowledge |
| Structured output | response constrained toward a schema | still validate types, ranges, and business rules |
| Tool calling | model proposes a named operation with arguments | Java code owns validation and execution |
| Agent | system where a model helps select actions across steps | autonomy is a design choice, not a synonym for chatbot |
| Guardrail | control that checks or constrains input, context, output, or action | defense in depth, not one regex |
| Prompt injection | untrusted content attempts to alter intended instructions | retrieved documents are untrusted too |
| Evaluation dataset | representative cases with expected behavior or scoring criteria | version it like test fixtures |
| Offline evaluation | repeatable evaluation outside live traffic | supports controlled comparison |
| Online evaluation | monitoring/experiments on real usage | needs privacy and rollback controls |
| Latency | elapsed time perceived by the caller | track distributions, not only averages |
| Rate limit | provider constraint on request/token throughput | requires backpressure and bounded retry |
| Idempotency | repeated execution has one intended effect | critical for tool calls with side effects |
| Adapter | translates a provider API/SDK into an application-owned interface | provider types stop at this boundary |
| Composition root | one place that constructs and connects application objects | explicit Core Java alternative to a DI container |
| Responses API | OpenAI API surface used by the official Java reference for generation | provider-specific; isolate behind a port |
