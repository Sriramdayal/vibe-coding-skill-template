# Python DSA Principles for Efficient Code

- **Time‑complexity targets**: Aim for O(n log n) or better; avoid O(n²) unless input size is provably tiny.  
- **Python Data‑Structure Cheat‑Sheet**:  
  - **Hash Set (`set`)** – O(1) average lookup/insert; use for duplicate detection, intersection (`&`), union (`|`).  
  - **Hash Map (`dict`, `defaultdict`, `Counter`)** – O(1) average key‑value access; standard `dict` for mapping, `collections.Counter` for frequency counting, `defaultdict` for grouping without `KeyError`.  
  - **Queues & Stacks (`collections.deque`)** – O(1) push/pop from both ends. Never use `list.pop(0)` as it is O(n).  
  - **Heap / Priority Queue (`heapq`)** – Min-heap by default. O(log n) insert/extract. Push negative values for a max-heap.  
  - **Binary Search (`bisect`)** – O(log n) searches in sorted lists. `bisect_left` / `bisect_right` are highly optimized.  
  - **Iteration Tools (`itertools`)** – Use `chain`, `combinations`, `permutations`, and `groupby` for optimized C-level iteration loops.
- **Algorithmic patterns (Python specific)**:  
  - **List/Dict/Set Comprehensions** – Usually faster than explicit `for` loops and `append()`.  
  - **Generators (`yield`)** – Use to keep memory footprint at O(1) when lazily evaluating large streams of data.  
  - **Memoization (`functools.cache` / `functools.lru_cache`)** – Instant Dynamic Programming cache without writing a distinct memo map.  
- **Golden rule**: Always ask the LLM to state the chosen complexity and Python standard library tools used in a comment above the function.
