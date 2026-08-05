# Day 1 Assignment — GenAI Use-Case Canvas

## Scenario

A company wants an “AI assistant” for one of these domains: HR onboarding, passport-document guidance, Java training support, or customer-service drafting.

## Deliverables

1. one-sentence user problem;
2. target users and the decision/task being improved;
3. inputs, authoritative sources, and expected output;
4. deterministic Java responsibilities;
5. model responsibility, limited to one bounded capability;
6. three unacceptable outcomes;
7. privacy classification for each input;
8. human-review or escalation rule;
9. provider-outage behavior;
10. Mermaid context diagram with at least two trust boundaries.

Add a Java 21 record that represents the use-case decision inputs. Mark it as a concept fragment and explain two validations not visible in the record declaration.

## Constraints

- Do not design a chatbot that “answers anything.”
- Do not allow the model to commit data or approve transactions.
- Do not use implementation code or real personal data.
- Include one reason the use case should be rejected or narrowed.

## Acceptance criteria

The model responsibility is generative, the Java responsibilities are deterministic, sources are identifiable, failure behavior is safe, and every risk has a proposed control or escalation path.

## Stretch question

How would the design change if the answer must be legally defensible six months later?

