# Final Assessment — Faculty Key

## Section A expected points

1. Temperature affects sampling where supported; truth depends on evidence/task/model and validation.
2. Prompting changes inference instructions; RAG adds retrieved evidence; fine-tuning changes behavior through additional training.
3. Instructions/history/input/evidence/output share a bounded context; application selects/truncates with priority.
4. Semantic finds meaning/paraphrase; lexical excels at exact terms; hybrid can combine.
5. Schema constrains shape; Java checks parse, fields, enums, ranges, business rules, citations, safety.
6. Tool call is a proposal; workflow is controlled steps; agent adds model-guided decisions/iteration.

## Section B rubric

- sealed hierarchy covers all named outcomes and exhaustive handling — 4;
- HTTP mapping is deliberate and does not expose provider internals — 3;
- validation/failure rationale — 3;
- diagram separates controller, application, port, adapter, validators — 5;
- provider types contained and composition explicit — 3;
- virtual-thread explanation correct — 3;
- limits, deadlines, rate limits, cancellation/backpressure named — 4.

## Section C rubric

- source/version/country/effective date/security metadata — 4;
- governed ingestion and authorized query pipelines — 4;
- safe no/conflict behavior — 3;
- Java citation validation against request evidence — 3;
- retrieval metrics such as recall@k/filter correctness — 3;
- answer/grounding/citation metrics — 3.

## Section D rubric

Award two marks each for ten requested controls when explanation includes where enforcement occurs. Model instructions alone receive no security-control credit.

## Section E rubric

- clear context/forces — 3;
- both alternatives fairly compared — 3;
- decision tied to team/use case — 3;
- consequences/risks — 2;
- review triggers — 2;
- Maven parent/BOM/release/version verification — 2.
