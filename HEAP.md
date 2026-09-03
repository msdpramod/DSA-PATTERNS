# Heap and Priority Queue Problems Segregated by Pattern

Recommended order: **Top-K → Repeated extraction → Scheduling → Resource assignment → Greedy heap → Two-heaps → Sweep line → Advanced heap DP/queries**.

> Some problems permit sorting, binary search, or other structures. Each appears under the heap pattern most useful for interview recognition.

## 1. Streaming Top-K

**Recognition:** Values arrive one by one, and the k-th largest must be available after every insertion.

**Core approach:** Maintain a min-heap of size `k`; its root is the current k-th largest.

- [Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/)

## 2. Static Top-K Selection

**Recognition:** Find the k-th largest/smallest item or retain only the best `k` items.

**Core approach:** Maintain a size-`k` heap, use a full heap, or apply quickselect when streaming behavior is unnecessary.

- [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/)
- [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)
- [Find the Kth Largest Integer in the Array](https://leetcode.com/problems/find-the-kth-largest-integer-in-the-array/)

## 3. Repeated Extreme Extraction

**Recognition:** Repeatedly remove the largest or smallest value, transform it, and insert a result.

**Core approach:** Store active values in a heap and simulate exactly `k` operations or until one value remains.

- [Last Stone Weight](https://leetcode.com/problems/last-stone-weight/)
- [Take Gifts From the Richest Pile](https://leetcode.com/problems/take-gifts-from-the-richest-pile/)
- [Final Array State After K Multiplication Operations I](https://leetcode.com/problems/final-array-state-after-k-multiplication-operations-i/)

## 4. Optimal Merge Pattern

**Recognition:** Combining two items costs their sum, and the combined result participates in later merges.

**Core approach:** Always merge the two smallest values first using a min-heap.

- [Minimum Cost to Connect Sticks](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)

## 5. Per-Group Top-K Aggregation

**Recognition:** Compute a top-`k) statistic independently for each group.

**Core approach:** Keep a bounded min-heap for every group, then aggregate the retained values.

- [High Five](https://leetcode.com/problems/high-five/)

## 6. Greedy Assignment by Ordered Priority

**Recognition:** Match two entity types using distance, cost, or another ordered preference with deterministic tie-breaking.

**Core approach:** Push candidate assignments into a priority queue or bucket them by priority and accept still-unassigned pairs.

- [Campus Bikes](https://leetcode.com/problems/campus-bikes/)

## 7. Frequency Heap and Cooldown Scheduling

**Recognition:** Repeated equal characters/tasks must be separated, or the most frequent valid choice should be used first.

**Core approach:** Use a max-heap of remaining frequencies plus a queue or temporary buffer for cooling items.

- [Rearrange String K Distance Apart](https://leetcode.com/problems/rearrange-string-k-distance-apart/)
- [Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- [Reorganize String](https://leetcode.com/problems/reorganize-string/)
- [Longest Happy String](https://leetcode.com/problems/longest-happy-string/)

## 8. Multiway Merge

**Recognition:** Merge several already ordered streams while producing only the next globally best item.

**Core approach:** Put one frontier item from each stream into a heap and advance only the stream whose item is removed.

- [Design Twitter](https://leetcode.com/problems/design-twitter/)

## 9. Remove Cheapest Frequencies First

**Recognition:** Remove a limited number of occurrences while minimizing the number of remaining distinct values.

**Core approach:** Count frequencies and remove the smallest frequency groups first with sorting or a min-heap.

- [Least Number of Unique Integers After K Removals](https://leetcode.com/problems/least-number-of-unique-integers-after-k-removals/)

## 10. Greedy Heap Replacement

**Recognition:** A scarce resource should be reserved for the most expensive choices encountered so far.

**Core approach:** Tentatively pay with the flexible resource, keep chosen costs in a heap, and replace/refund when the constrained budget is exceeded.

- [Furthest Building You Can Reach](https://leetcode.com/problems/furthest-building-you-can-reach/)

## 11. Normalize and Reduce the Current Maximum

**Recognition:** Values can be transformed into ranges, and the goal is to minimize the current maximum-minus-minimum deviation.

**Core approach:** Normalize values upward first, then repeatedly reduce the maximum while tracking the minimum.

- [Minimize Deviation in Array](https://leetcode.com/problems/minimize-deviation-in-array/)

## 12. Sort One Dimension + Maintain Best K

**Recognition:** A score combines a selected sum with the minimum/maximum of another property.

**Core approach:** Sort by the constraining property, maintain the best `k` complementary values in a heap, and evaluate each boundary.

- [Maximum Subsequence Score](https://leetcode.com/problems/maximum-subsequence-score/)
- [Maximum Performance of a Team](https://leetcode.com/problems/maximum-performance-of-a-team/)
- [Minimum Cost to Hire K Workers](https://leetcode.com/problems/minimum-cost-to-hire-k-workers/)

## 13. Event Scheduling with Availability Heap

**Recognition:** Tasks arrive over time, and the next task is chosen by duration or priority.

**Core approach:** Sort arrivals, jump time when idle, and keep all currently available tasks in a priority queue.

- [Single-Threaded CPU](https://leetcode.com/problems/single-threaded-cpu/)

## 14. Resource Allocation with One or Two Heaps

**Recognition:** Assign the smallest/best available resource and return it when released.

**Core approach:** Maintain available resources in one heap and busy resources ordered by release time in another.

- [Seat Reservation Manager](https://leetcode.com/problems/seat-reservation-manager/)
- [Process Tasks Using Servers](https://leetcode.com/problems/process-tasks-using-servers/)

## 15. Capacity Timeline and Sweep Line

**Recognition:** Resource usage changes at interval endpoints and must never exceed capacity.

**Core approach:** Record signed changes in a difference structure or process starts and ends in order.

- [Car Pooling](https://leetcode.com/problems/car-pooling/)

## 16. Two Heaps for Running Median

**Recognition:** Insert values online and query the median repeatedly.

**Core approach:** Keep the lower half in a max-heap and upper half in a min-heap; rebalance their sizes after insertion.

- [Find Median From Data Stream](https://leetcode.com/problems/find-median-from-data-stream/)

## 17. Capital-Constrained Project Selection

**Recognition:** Each selected project changes the budget and unlocks more choices.

**Core approach:** Sort projects by required capital; move affordable projects into a max-heap of profits.

- [IPO](https://leetcode.com/problems/ipo/)

## 18. Interval Queries by Sorted Endpoints

**Recognition:** Count active intervals at many query times.

**Core approach:** Sort starts and ends separately and use binary search, or sweep queries while maintaining active endpoints.

- [Number of Flowers in Full Bloom](https://leetcode.com/problems/number-of-flowers-in-full-bloom/)

## 19. Heap over Generated Subarray Values

**Recognition:** Subarray sums form ordered sequences that can be generated incrementally.

**Core approach:** Treat each start index as a sorted stream of expanding subarray sums and perform a k-way merge.

- [Range Sum of Sorted Subarray Sums](https://leetcode.com/problems/range-sum-of-sorted-subarray-sums/)

## 20. Greedy Transaction Ordering

**Recognition:** Maximize how many transactions can be completed without the running balance becoming negative.

**Core approach:** Process candidates and use a heap to discard the most damaging selected transaction when feasibility breaks.

- [Maximum Transactions Without Negative Balance](https://leetcode.com/problems/maximum-transactions-without-negative-balance/)

## 21. Maximum-Capacity Grid Path

**Recognition:** Path quality equals the minimum cell value along it, and that value must be maximized.

**Core approach:** Use a max-heap; always expand the currently safest frontier and track the minimum value along the path.

- [Path With Maximum Minimum Value](https://leetcode.com/problems/path-with-maximum-minimum-value/)

## 22. Monotonic Heap / Window DP

**Recognition:** The best DP predecessor must lie within the previous `k` indices.

**Core approach:** Maintain candidate DP values in decreasing order with a deque; a heap with lazy expiry is an alternative.

- [Constrained Subsequence Sum](https://leetcode.com/problems/constrained-subsequence-sum/)

## 23. Offline Queries with a Frontier Heap

**Recognition:** Each query asks for the first valid structure to the right that exceeds a threshold.

**Core approach:** Sort queries by the point at which they become answerable and maintain unresolved thresholds in a heap.

- [Find Building Where Alice and Bob Can Meet](https://leetcode.com/problems/find-building-where-alice-and-bob-can-meet/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| K-th value in a stream | Size-K heap |
| Static K-th/top-K | Heap or quickselect |
| Repeatedly modify largest/smallest | Extreme-value heap |
| Merge cost equals combined size | Optimal merge min-heap |
| Separate repeated tasks | Frequency heap + cooldown |
| Merge ordered feeds | K-way merge |
| Reuse earliest available resource | Availability/busy heaps |
| Task arrivals plus processing priority | Event sorting + heap |
| Running median | Two heaps |
| Budget unlocks profitable choices | Capital sort + profit heap |
| Select K while sweeping a constraint | Sort + bounded heap |
| DP maximum over last K positions | Monotonic deque |
| Answer threshold queries offline | Sorted queries + heap |

## Recommended Practice Order

1. Kth Largest Element in a Stream
2. Last Stone Weight
3. K Closest Points
4. Minimum Cost to Connect Sticks
5. Task Scheduler and Reorganize String
6. Furthest Building
7. Single-Threaded CPU
8. Seat Reservation and Server Assignment
9. Find Median From Data Stream
10. Maximum Performance and Worker Hiring
11. IPO and interval queries
12. Constrained Subsequence Sum and offline frontier queries
