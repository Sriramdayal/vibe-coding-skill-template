---
name: vibe-coding-guidelines-python
description: Use when starting a new Python feature or writing code with vibe coding to ensure efficient, DSA‑aware, and Pythonic output.
---
# Python Vibe Coding Guidelines

## When to Use
- You begin a new Python file, function, module, or class.  
- You want the agent to generate Pythonic code that follows PEP 8, uses appropriate typing, and leverages Python's standard library for optimal data‑structures.  

## What This Skill Does
1. **Load reference files** – `references/dsa-principles.md`, `references/prompting-tips.md`, `references/sdlc-guidelines.md`, and `references/context-engineering.md`.  
2. **Apply DSA & Python constraints** – Prefer O(n log n) or better. Use built-ins like `set()`, `dict()`, `collections.defaultdict`, `collections.deque`, and `heapq`. Avoid unnecessary loops if `itertools` or comprehensions work better.  
3. **Enforce vibe‑coding style** – Keep prompts short and context‑rich. Ensure all generated code includes strict type hints and Google/NumPy-style docstrings.  
4. **Output specification** – Return a Python code block satisfying the request, strict type checks, and optimal DSA, optionally followed by a brief explanation of the algorithms used.  

## How to Use
- Trigger the skill by typing `/skill vibe-coding-guidelines-python`.  
- The agent will follow the steps above, pulling in the reference files automatically.  

## Example
**User prompt**: “Write a function that returns the longest substring without repeating characters.”  
**Agent output** (after applying the skill):
```python
def longest_unique_substring(s: str) -> str:
    # Sliding window with a set for O(n) time, O(k) space
    char_set: set[str] = set()
    left = 0
    best = ""
    for right, ch in enumerate(s):
        while ch in char_set:
            char_set.remove(s[left])
            left += 1
        char_set.add(ch)
        if right - left + 1 > len(best):
            best = s[left:right+1]
    return best
```
