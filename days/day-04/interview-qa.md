# Day 4 Interview Questions and Answers

1. **Why hide provider SDK types behind an interface?**  
   It prevents provider coupling from spreading and makes application behavior testable with a deterministic substitute.

2. **When might raw `HttpClient` be appropriate?**  
   When protocol control, dependency minimization, or unsupported SDK features matter and the team accepts manual mapping/maintenance.

3. **Where should an API key be stored?**  
   In approved secret management or injected environment configuration, never source code or committed config.

4. **Which failures are normally retryable?**  
   Classified transient rate-limit, timeout, connection, or server failures—within a bounded deadline and attempt policy.

5. **Why use jitter?**  
   It reduces synchronized retry spikes from many callers after a shared failure.

6. **What is retry amplification?**  
   Multiple layers each retry, multiplying downstream attempts and worsening an outage.

7. **Why keep a total request deadline?**  
   Per-operation timeouts alone can accumulate beyond the caller’s acceptable latency.

8. **What should a provider response mapper preserve?**  
   Required content, request/correlation identity, usage and operational metadata, while translating provider-specific shapes.

9. **Is HTTP 200 a successful business result?**  
   Not necessarily. The content may be refused, malformed, ungrounded, or fail business validation.

10. **How can the service layer be tested without cost?**  
    Inject a stub/fake implementation of the provider-neutral port and test deterministic decisions.

