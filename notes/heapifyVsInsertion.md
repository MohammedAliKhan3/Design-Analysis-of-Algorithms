# Heapify vs Heap Insertion

| Aspect                      | Heapify (Bottom-Up)                                                                 | Heap Insertion (Top-Down)                                                                 |
|-----------------------------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| **Definition**              | Builds a heap from an existing array in a single pass (bottom-up adjustment).        | Inserts elements one by one into an empty heap, adjusting after each insert.             |
| **How it works**            | Starts from last non-leaf node, pushes down ("percolates down") to satisfy heap property. | Places new element at the end, then bubbles it up ("percolates up") to correct position. |
| **Time Complexity**         | O(n) overall for building a heap.                                                   | O(n log n) for inserting n elements (each insert costs O(log n)).                        |
| **Memory usage**            | In-place, no extra memory needed.                                                   | In-place, no extra memory needed.                                                        |
| **Best for**                | Converting an existing unsorted array into a heap quickly (e.g., Heap Sort).         | Maintaining a heap when elements arrive one-by-one (e.g., priority queue).               |
| **When not ideal**          | Not useful if elements arrive dynamically over time.                                | Less efficient if you already have all the elements from the start.                      |
| **Example use case**        | Heap Sort, initializing a heap from a dataset.                                      | Real-time scheduling, priority queue with dynamic input.                                 |

## Which is Better?

- **If you already have all the elements at once** → Heapify is better (O(n))
- **If you receive elements one by one over time** → Heap Insertion is better (maintains heap incrementally)

### 💡 Rule of Thumb
> **Use Heapify for batch creation**,  
> **Use Insertion for dynamic updates**.