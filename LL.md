# Linked List Problems Segregated by Pattern

Recommended order: **Traversal → Dummy node → Reversal → Fast/slow pointers → Two-pointer alignment → Merge/sort → Splicing → Design problems**.

> Some problems fit several categories. Each appears under the pointer pattern most useful for recognizing its primary solution.

## 1. Basic Traversal and Local Rewriting

**Recognition:** Inspect each node once and modify links or values using only local information.

**Core approach:** Walk with `current` and preserve `next` before changing any pointer.

- [Remove Duplicates From Sorted List](https://leetcode.com/problems/remove-duplicates-from-sorted-list/)
- [Delete N Nodes After M Nodes of a Linked List](https://leetcode.com/problems/delete-n-nodes-after-m-nodes-of-a-linked-list/)
- [Merge Nodes in Between Zeros](https://leetcode.com/problems/merge-nodes-in-between-zeros/)
- [Find the Minimum and Maximum Number of Nodes Between Critical Points](https://leetcode.com/problems/find-the-minimum-and-maximum-number-of-nodes-between-critical-points/)

## 2. Dummy-Head Deletion

**Recognition:** Nodes matching a condition may include the original head.

**Core approach:** Attach a dummy before the head and let `previous` decide whether to bypass `current`.

- [Remove Linked List Elements](https://leetcode.com/problems/remove-linked-list-elements/)
- [Delete Nodes From Linked List Present in Array](https://leetcode.com/problems/delete-nodes-from-linked-list-present-in-array/)
- [Remove Duplicates From an Unsorted Linked List](https://leetcode.com/problems/remove-duplicates-from-an-unsorted-linked-list/)

## 3. Whole-List Reversal

**Recognition:** Reverse every pointer or consume nodes in reverse order.

**Core approach:** Iteratively maintain `previous`, `current`, and `next`; recursion or divide-and-conquer is needed when nodes are immutable.

- [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- [Print Immutable Linked List in Reverse](https://leetcode.com/problems/print-immutable-linked-list-in-reverse/)

## 4. Partial and Group Reversal

**Recognition:** Reverse only a position range or fixed-size groups.

**Core approach:** Locate the node before the segment, reverse exactly the required nodes, then reconnect both boundaries.

- [Reverse Linked List II](https://leetcode.com/problems/reverse-linked-list-ii/)
- [Reverse Nodes in K-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/)
- [Swap Nodes in Pairs](https://leetcode.com/problems/swap-nodes-in-pairs/)

## 5. Fast and Slow Pointers

**Recognition:** Find the middle, detect a cycle, or detect repetition without extra memory.

**Core approach:** Move one pointer one step and another two steps; reason about where they meet.

- [Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/)
- [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- [Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/)

## 6. Offset Two Pointers

**Recognition:** Find a node relative to the end in one pass.

**Core approach:** Move the fast pointer ahead by a fixed gap, then advance both pointers together.

- [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)

## 7. Pointer Alignment and Shared Tail

**Recognition:** Two lists have different prefix lengths but may share the same tail nodes.

**Core approach:** Switch each pointer to the other head at the end, equalizing the total distance traveled.

- [Intersection of Two Linked Lists](https://leetcode.com/problems/intersection-of-two-linked-lists/)

## 8. Split, Reverse, and Compare/Combine Halves

**Recognition:** Pair symmetric nodes, test a palindrome, or interleave the two halves.

**Core approach:** Find the middle, reverse the second half, then compare or merge the halves.

- [Palindrome Linked List](https://leetcode.com/problems/palindrome-linked-list/)
- [Reorder List](https://leetcode.com/problems/reorder-list/)
- [Maximum Twin Sum of a Linked List](https://leetcode.com/problems/maximum-twin-sum-of-a-linked-list/)

## 9. Node Selection by Position

**Recognition:** Swap or identify nodes counted from opposite ends without changing their values' surrounding structure.

**Core approach:** Locate the first positional node, then use a trailing pointer to locate the corresponding node from the end.

- [Swapping Nodes in a Linked List](https://leetcode.com/problems/swapping-nodes-in-a-linked-list/)

## 10. Merge Sorted Lists

**Recognition:** Input lists are individually sorted and must produce one sorted list.

**Core approach:** Use a dummy tail for two lists; for `k` lists use divide-and-conquer or a min-heap.

- [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- [Merge K Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)

## 11. Linked-List Sorting

**Recognition:** Sort nodes while preserving linked-list structure.

**Core approach:** Use merge sort for `O(n log n)`; insertion sort is useful when the problem explicitly requests or benefits from incremental insertion.

- [Sort List](https://leetcode.com/problems/sort-list/)
- [Insertion Sort List](https://leetcode.com/problems/insertion-sort-list/)

## 12. Stable Partitioning

**Recognition:** Rearrange nodes into groups while preserving original relative order within each group.

**Core approach:** Build separate dummy-headed lists and connect them at the end.

- [Partition List](https://leetcode.com/problems/partition-list/)

## 13. Splicing and Segment Replacement

**Recognition:** Remove a contiguous segment and insert another list at that position.

**Core approach:** Locate the node before the removed segment and its successor, then connect the replacement list's head and tail.

- [Merge in Between Linked Lists](https://leetcode.com/problems/merge-in-between-linked-lists/)

## 14. Rotation and Splitting by Length

**Recognition:** Shift nodes cyclically or divide a list into nearly equal consecutive parts.

**Core approach:** Compute length first; use modular arithmetic for rotation or quotient/remainder sizes for splitting.

- [Rotate List](https://leetcode.com/problems/rotate-list/)
- [Split Linked List in Parts](https://leetcode.com/problems/split-linked-list-in-parts/)

## 15. Monotonic Filtering

**Recognition:** Remove nodes that have a greater value somewhere to their right.

**Core approach:** Reverse the list and retain a running maximum, or use a monotonic stack.

- [Remove Nodes From Linked List](https://leetcode.com/problems/remove-nodes-from-linked-list/)

## 16. Circular Linked Lists

**Recognition:** There is no null tail, and insertion must preserve a cyclic sorted order.

**Core approach:** Traverse until finding the normal sorted gap, the maximum-to-minimum wrap point, or returning to the start.

- [Insert into a Sorted Circular Linked List](https://leetcode.com/problems/insert-into-a-sorted-circular-linked-list/)

## 17. Arithmetic with Carry

**Recognition:** Each node stores a digit and arithmetic must be performed in list order.

**Core approach:** Traverse least-significant digits directly; for forward-order digits use stacks, recursion, or reversal.

- [Plus One Linked List](https://leetcode.com/problems/plus-one-linked-list/)
- [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/)
- [Add Two Numbers II](https://leetcode.com/problems/add-two-numbers-ii/)

## 18. Clone with Random Pointers

**Recognition:** Nodes contain both sequential and arbitrary cross-links.

**Core approach:** Map originals to copies, or interleave copied nodes with originals to achieve constant auxiliary space.

- [Copy List With Random Pointer](https://leetcode.com/problems/copy-list-with-random-pointer/)

## 19. Pointer-Based Data-Structure Design

**Recognition:** Implement indexed navigation, bidirectional history, or circular storage.

**Core approach:** Choose singly linked, doubly linked, or circular-array/list structure based on required operations.

- [Design Linked List](https://leetcode.com/problems/design-linked-list/)
- [Design Browser History](https://leetcode.com/problems/design-browser-history/)
- [Design Circular Queue](https://leetcode.com/problems/design-circular-queue/)

## 20. Hash Map + Doubly Linked List Caches

**Recognition:** Reads and updates must be `O(1)` while evicting by recency or frequency.

**Core approach:** Map keys to nodes and maintain ordered doubly linked lists; LFU additionally maps each frequency to its own recency list.

- [LRU Cache](https://leetcode.com/problems/lru-cache/)
- [LFU Cache](https://leetcode.com/problems/lfu-cache/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Head may be removed | Dummy node |
| Reverse all links | Three pointers |
| Reverse a segment/group | Boundary reconnect |
| Middle or cycle | Fast/slow pointers |
| N-th node from end | Fixed-gap pointers |
| Shared tail of two lists | Pointer switching |
| Symmetric node pairs | Split + reverse second half |
| Merge sorted lists | Dummy tail or min-heap |
| Sort a linked list | Merge sort |
| Preserve order across partitions | Multiple dummy lists |
| Greater value on the right | Reverse + running maximum |
| Forward-order digit arithmetic | Stack or reversal |
| Random cross-links | Original-to-copy mapping |
| O(1) cache eviction | Hash map + doubly linked list |

## Recommended Practice Order

1. Reverse Linked List
2. Merge Two Sorted Lists
3. Middle and Cycle Detection
4. Remove Nodes with a Dummy Head
5. Remove Nth Node From End
6. Palindrome, Twin Sum, and Reorder List
7. Partial and K-Group Reversal
8. Sort and Merge K Lists
9. Arithmetic and Random Pointer Copy
10. Circular lists and stable partitioning
11. LRU Cache
12. LFU Cache
