## Summary

Heap Sort is a comparison-based sorting algorithm that uses a **binary heap** data structure to sort elements. It first builds a **Max Heap**, where the largest element is placed at the root. The root element is then swapped with the last element, the heap size is reduced, and the heap is rearranged using the heapify operation. This process is repeated until all elements are sorted.

**Time Complexity:**

* Best Case: O(n log n)
* Average Case: O(n log n)
* Worst Case: O(n log n)

**Space Complexity:** O(1) auxiliary space
**Stability:** Not stable

## Conclusion

Heap Sort is an efficient and reliable sorting algorithm with a guaranteed **O(n log n)** time complexity in all cases. Since it sorts the elements in-place and does not require additional memory proportional to the input size, it is useful when memory efficiency is important. However, compared with algorithms such as Quick Sort, Heap Sort may have poorer practical performance due to less favorable cache behavior.
