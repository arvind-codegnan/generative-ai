# Day 8 Assignment — Safe Tool Workflow

## Scenario

Design an employee helpdesk assistant that can search knowledge articles, retrieve a ticket, draft an update, and propose closing the ticket. Only a human agent may approve closure.

## Deliverables

- tool catalog with input/output schemas and side-effect levels;
- trusted `ExecutionContext` design;
- state diagram from proposal through approval/execution;
- authorization matrix by user role;
- idempotency design for ticket closure;
- timeout, step, call, and cost budgets;
- tool-result injection controls;
- audit-event record sketches;
- 12 test scenarios including retries and denied approval;
- explanation of which steps remain deterministic and why.

## Required failure cases

- model proposes an unknown tool;
- ticket ID belongs to another tenant;
- approval expires;
- closure succeeds but response times out;
- model repeats the same closure call;
- retrieved article contains “ignore all rules”;
- human changes ticket state before approval.

## Acceptance criteria

The model cannot create identity or approval, side effects are idempotent, workflow state is durable, and the system stops safely on non-progress or budget exhaustion.

