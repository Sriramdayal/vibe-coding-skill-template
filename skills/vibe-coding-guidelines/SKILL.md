---
name: vibe-coding-guidelines
description: Use when starting a new feature or writing code with vibe coding to ensure efficient, DSA‑aware output.
---
# Vibe Coding Guidelines

## When to Use
- You begin a new file, function, or module.  
- You want the agent to generate code that follows optimal data‑structure choices and complexity targets.  

## What This Skill Does
1. **Load reference files** – `references/dsa-principles.md` and `references/prompting-tips.md`.  
2. **Apply DSA constraints** – Prefer O(n log n) or better; use `Set`/`Map` for look‑ups; avoid nested loops unless unavoidable.  
3. **Enforce vibe‑coding style** – Keep prompts short, iterative, and context‑rich; validate each AI‑generated increment before proceeding.  
4. **Output specification** – Return a code block that satisfies the functional request *and* the DSA constraints, optionally followed by a brief explanation of the chosen algorithm/data structure.  

## How to Use
- Trigger the skill by typing `/skill vibe-coding-guidelines` (or however your agent invokes skills).  
- The agent will follow the steps above, pulling in the reference files automatically.  

## Example
**User prompt**: “Write a function that returns the longest substring without repeating characters.”  
**Agent output** (after applying the skill):
```python
def longest_unique_substring(s: str) -> str:
    # Sliding window with a set for O(n) time, O(k) space
    char_set = set()
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
