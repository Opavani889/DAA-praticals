Summary of sorting algorithms

Bubble sort

Idea: Repeatedly sweep through the list, swapping adjacent out-of-order elements until no swaps are needed.
Complexity: Best O(n) (already sorted, with optimization), Average/Worst O(n^2)
Space: O(1) (in-place)
Stability: Stable
When to use: Teaching/illustration, tiny or nearly-sorted lists (rare in practice)
Pros/Cons: Very simple, but inefficient for large lists.

Selection sort

Idea: Repeatedly find the minimum (or maximum) element from the unsorted portion and swap it into place.
Complexity: Best/Average/Worst O(n^2)
Space: O(1) (in-place)
Stability: Not stable by default (can be made stable with extra work)
When to use: Very small arrays or when minimizing writes matters (it does at most n swaps)
Pros/Cons: Predictable number of swaps, but slow for large n.

Insertion sort

Idea: Build the sorted array one element at a time by inserting each new element into its correct position in the sorted prefix.
Complexity: Best O(n) (already or nearly sorted), Average/Worst O(n^2)
Space: O(1) (in-place)
Stability: Stable
When to use: Small arrays, nearly-sorted data, as the base case for hybrid algorithms (e.g., Timsort)
Pros/Cons: Simple and efficient on small/partially-sorted inputs.

Merge sort

Idea: Divide the array in half, recursively sort each half, then merge the sorted halves.
Complexity: Best/Average/Worst O(n log n)
Space: O(n) extra (standard array-based implementation); O(log n) for linked-list variants
Stability: Stable (standard implementation)
When to use: Large data, when stable sort is required, external sorting (can be adapted)
Pros/Cons: Predictable O(n log n) time and stable, but uses extra memory.

Quick sort

Idea: Pick a pivot, partition the array into elements less-than and greater-than the pivot, recursively sort partitions.
Complexity: Average O(n log n), Worst O(n^2) (rare with good pivot strategy)
Space: O(log n) expected recursion stack (in-place partitioning)
Stability: Not stable by default
When to use: General-purpose in-memory sorting of arrays; often fastest in practice with good pivoting and hybridization
Pros/Cons: Very fast average-case and low overhead, but watch for worst-case and lack of stability.

Conclusion (how to choose)
For production code, prefer your language's built-in sort (Python uses Timsort) — it is optimized (stable, adaptive, O(n log n) worst-case) and handles many edge cases.
If you need a stable algorithm and can afford extra memory, use Merge Sort (or Timsort hybrid).
For in-place, average-fast performance on arrays, Quick Sort (with randomized pivot or introsort fallback) is a strong choice.
For small arrays (typical cutoff ~10–64 elements), Insertion Sort often outperforms O(n log n) algorithms due to low overhead; hybrids use this fact.
Selection and Bubble sorts are primarily educational: they demonstrate basic ideas but are generally too slow for real workloads (selection sort can be useful when writes are very expensive).
Always weigh: input size, memory constraints, stability requirement, and whether data is nearly sorted.
