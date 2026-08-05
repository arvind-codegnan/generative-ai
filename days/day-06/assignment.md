# Day 6 Assignment — Semantic Search Design

## Scenario

Index an employee handbook containing global policies and country-specific annexures.

## Deliverables

- chunking strategy with size/overlap rationale;
- `KnowledgeChunk`, `EmbeddedChunk`, `SearchFilter`, and `SearchHit` record sketches;
- vector-store port;
- metadata catalog including tenant, country, document version, effective dates, section, and security label;
- hybrid retrieval diagram;
- 12-query retrieval evaluation set, including exact policy codes and paraphrases;
- embedding-model migration plan;
- deletion/update flow when a policy is superseded.

## Required edge cases

- two countries use conflicting leave rules;
- a new document version is effective next month;
- a query contains an exact form ID;
- no authorized chunk meets the threshold;
- the same paragraph appears in several documents.

## Acceptance criteria

The design prevents cross-region leakage, preserves citation identity, supports lifecycle operations, and evaluates retrieval separately from final answer quality.

