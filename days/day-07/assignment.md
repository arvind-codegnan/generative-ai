# Day 7 Assignment — Citation-Backed RAG Architecture

## Scenario

Design a question-answering service over company travel policies. Policies vary by grade, country, and effective date.

## Deliverables

- ingestion and query diagrams;
- document approval/update/deletion process;
- chunk and citation contracts;
- access-scope and retrieval-budget types;
- grounded prompt specification;
- sealed RAG result hierarchy;
- citation-validation algorithm in prose;
- failure matrix for every pipeline stage;
- 15-case end-to-end evaluation set;
- Core Java port/adapter mapping for loaders, chunking, embeddings, index and retrieval.

## Required cases

- conflicting current documents;
- no evidence;
- prompt injection in a policy document;
- unauthorized country policy;
- source is replaced after retrieval;
- valid answer cites the wrong chunk;
- relevant chunk ranked sixth when top-k is five.

## Acceptance criteria

The design provides source traceability, fails safely without evidence, enforces access before generation, and distinguishes retrieval, generation, and citation quality.
