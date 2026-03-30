# Effective Python Vibe‑Coding Prompts

1. **Be specific about the goal** – “Create a FastAPI endpoint that returns paginated user events.”  
2. **State performance & memory constraints** – “Ensure the generator yields items one at a time to keep memory at O(1).”  
3. **Mention Python-specific libraries/patterns** – “Use `itertools.groupby` instead of a manual for-loop, and apply `@lru_cache` for memoization.”  
4. **Enforce Type Hinting & Linters** – “Add strict type hints (`typing.List`, `typing.Optional`, etc.) and ensure it passes `mypy --strict`.”  
5. **Ask for Testing Boilerplate** – “Include a `pytest` block at the bottom using `pytest.mark.parametrize`.”  
6. **Iterate** – Review the AI’s output, then give a follow‑up prompt like “Replace the `list.pop(0)` with `collections.deque` for O(1) left-pops.”  
7. **Leverage the agent’s tools** – Ask the agent to run `pytest`, `ruff`, or `mypy` locally before it delivers the final snippet.
