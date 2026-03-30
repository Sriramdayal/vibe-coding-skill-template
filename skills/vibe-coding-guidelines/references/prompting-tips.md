# Effective Vibe‑Coding Prompts

1. **Be specific about the goal** – “Create a REST endpoint that returns paginated user events.”  
2. **State performance constraints** – “Expected ≤ 10 k events/sec, latency < 20 ms, memory < 50 MB.”  
3. **Mention data‑structure preferences** – “Use a hash set for duplicate detection to achieve O(1) look‑up.”  
4. **Ask for complexity comments** – “Include a comment that specifies the time and space complexity.”  
5. **Iterate** – Review the AI’s output, then give a follow‑up prompt like “Replace the nested loop with a sliding‑window approach.”  
6. **Provide context** – Paste relevant type definitions or a snippet of existing code so the model grounds its answer.  
7. **Leverage the agent’s tools** – Ask the agent to run unit tests, lint, or benchmark the generated code before accepting it.  
