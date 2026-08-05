# Day 8 Interview Questions and Answers

1. **Does a model execute a tool?**  
   It normally proposes a tool and arguments; trusted application code validates and executes.

2. **Why keep execution context out of model arguments?**  
   Identity, tenant, permissions, and approval must come from trusted application state.

3. **What is idempotency?**  
   Repeating the same approved request has one intended effect or safely returns the existing result.

4. **When is a deterministic workflow better than an agent?**  
   When steps and conditions are known and auditability/reliability matter more than flexible model choice.

5. **Why separate draft-email and send-email tools?**  
   Drafting is reversible generation; sending creates an external side effect and needs recipient/approval checks.

6. **What should terminate an agent loop?**  
   Success, policy denial, inability, deadline, budget exhaustion, repeated failure, or lack of progress.

7. **Is tool output trusted?**  
   No. It can contain malicious or misleading content and must be treated as data.

8. **What must be audited?**  
   Proposal, arguments after validation, identity/authorization decision, approval, execution, result, and failures—subject to privacy.

9. **Can read-only tools leak data?**  
   Yes. Retrieval must enforce tenant, field, record, and purpose restrictions.

10. **What does a plain Java tool registry not provide automatically?**  
    Complete authorization, approval, least privilege, idempotency, safe result handling, or domain policy.
