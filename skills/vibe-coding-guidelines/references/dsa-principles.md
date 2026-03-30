# DSA Principles for Efficient Code

- **Time‑complexity targets**: Aim for O(n log n) or better; avoid O(n²) unless input size is provably tiny.  
- **Data‑structure cheat‑sheet**:  
  - **Hash Set** – O(1) average lookup/insert; use for duplicate detection, membership tests.  
  - **Hash Map** – O(1) average key‑value access; use for caching, counting, ID‑based look‑ups.  
  - **Balanced BST (e.g., Red‑Black Tree, AVL)** – O(log n) ordered operations; use when you need sorted keys or range queries.  
  - **Heap (Min/Max)** – O(log n) insert/extract‑min/max; use for priority queues, streaming top‑k.  
  - **Union‑Find (Disjoint Set)** – Near‑constant amortized time; use for connectivity / Kruskal’s MST.  
  - **Trie** – O(L) per string operation (L = key length); use for prefix‑based searches, autocomplete.  
- **Algorithmic patterns**:  
  - **Sliding window** – O(n) for subarray/substring problems with monotonic constraints.  
  - **Two‑pointer** – O(n) for sorted arrays, palindrome checks, sum‑to‑target.  
  - **Divide‑and‑conquer** – O(n log n) (merge sort, quick‑sort average).  
  - **Dynamic programming** – O(n·m) when subproblems overlap; prefer memoisation over naïve recursion.  
- **Space‑time trade‑offs**: Prefer extra O(n) space if it reduces time from O(n²) to O(n log n) or O(n).  
- **Golden rule**: Always ask the LLM to state the chosen complexity and data structure in a comment above the function.  
