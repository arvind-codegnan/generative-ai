# Primary References

Version-sensitive claims were checked on 2026-08-05. Verify current documentation before implementation.

## Java and Maven

- [Java 21 documentation](https://docs.oracle.com/en/java/javase/21/)
- [Java HTTP Client](https://docs.oracle.com/en/java/javase/21/docs/api/java.net.http/java/net/http/HttpClient.html)
- [Java virtual threads](https://docs.oracle.com/en/java/javase/21/core/virtual-threads.html)
- [Maven lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)
- [Maven Compiler Plugin `--release`](https://maven.apache.org/plugins/maven-compiler-plugin/examples/set-compiler-release.html)

## OpenAI concrete-provider references

- [OpenAI SDKs and Java helper](https://developers.openai.com/api/docs/libraries)
- [OpenAI Java API reference](https://developers.openai.com/api/reference/java/)
- [Responses API](https://developers.openai.com/api/reference/resources/responses/)
- [Prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering)
- [Structured outputs](https://developers.openai.com/api/docs/guides/structured-outputs)
- [Embeddings](https://developers.openai.com/api/docs/guides/embeddings)
- [Function calling](https://developers.openai.com/api/docs/guides/function-calling)
- [Safety best practices](https://developers.openai.com/api/docs/guides/safety-best-practices)

## Reading rule

Identify the provider-neutral concept first. Then verify the current SDK/API shape, model capability, account availability, data policy, limits, and error behavior. Never treat a training fragment as current production configuration.

