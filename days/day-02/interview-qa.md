# Day 2 Interview Questions and Answers

1. **Is a token the same as a word?**  
   No. A token may be a word, word piece, punctuation, or another unit chosen by the tokenizer.

2. **What occupies the context window?**  
   Instructions, messages/history, user input, retrieved content, tool results, reserved output, and protocol overhead.

3. **Is context a model’s permanent memory?**  
   No. It is bounded input for a request. The application manages durable state and selected history.

4. **What does self-attention achieve intuitively?**  
   It lets token representations use relevant information from other positions to become context-aware.

5. **What is an embedding?**  
   A numeric representation used to compare semantic characteristics of content.

6. **Why clone a `float[]` inside a Java record?**  
   Records make references final, not the referenced array immutable. Cloning prevents external mutation.

7. **Does temperature measure confidence?**  
   No. Where supported, it adjusts sampling variation; it does not certify correctness.

8. **Why reserve output tokens?**  
   Filling the entire context with input can leave insufficient room for the required response.

9. **Do virtual threads solve rate limits?**  
   No. They reduce blocked-thread cost; quotas and downstream capacity still require limits and backpressure.

10. **Why log prompt and model versions for evaluation?**  
    Without configuration identity, output changes cannot be reproduced, compared, or diagnosed responsibly.

