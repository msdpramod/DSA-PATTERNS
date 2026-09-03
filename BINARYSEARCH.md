# Binary Search Problems Segregated by Pattern

Recommended order: **Exact search → Bounds → Rotated arrays → Peaks → Integer answer search → Real-valued search → K-th element search**.

> Some problems admit several techniques. Each appears under the binary-search pattern most useful for recognizing its primary solution.

## 1. Classic Exact Binary Search

**Recognition:** Find a target in a sorted or monotonic search space.

**Core approach:** Compare the middle value with the target and discard half of the remaining range.

- [Binary Search](https://leetcode.com/problems/binary-search/)
- [Guess Number Higher or Lower](https://leetcode.com/problems/guess-number-higher-or-lower/)

## 2. Lower Bound and Insertion Position

**Recognition:** Find the first index whose value is at least a target.

**Core approach:** Use a half-open interval and preserve the first potentially valid position.

- [Search Insert Position](https://leetcode.com/problems/search-insert-position/)

## 3. First/Last Occurrence and Frequency

**Recognition:** Find an equal-value range or determine how many times a target appears in sorted data.

**Core approach:** Run separate lower-bound and upper-bound searches.

- [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- [Check If a Number Is Majority Element in a Sorted Array](https://leetcode.com/problems/check-if-a-number-is-majority-element-in-a-sorted-array/)

## 4. Binary Search on Numeric Values

**Recognition:** Find an integer root, triangular count, or greatest value satisfying an arithmetic inequality.

**Core approach:** Search the numeric answer range and avoid overflow when evaluating the predicate.

- [Arranging Coins](https://leetcode.com/problems/arranging-coins/)
- [Valid Perfect Square](https://leetcode.com/problems/valid-perfect-square/)
- [Sqrt(x)](https://leetcode.com/problems/sqrtx/)

## 5. Missing Value in Ordered Structure

**Recognition:** A sorted progression has missing values, and the number missing before index `i` is monotonic.

**Core approach:** Derive the expected value or missing-count function and locate the first index crossing the target.

- [Missing Number in Arithmetic Progression](https://leetcode.com/problems/missing-number-in-arithmetic-progression/)
- [Missing Element in Sorted Array](https://leetcode.com/problems/missing-element-in-sorted-array/)

## 6. Parity-Based Binary Search

**Recognition:** Sorted pairs occupy predictable even/odd positions except around one unique element.

**Core approach:** Align the midpoint to a pair boundary and choose the half where the parity pattern breaks.

- [Single Element in a Sorted Array](https://leetcode.com/problems/single-element-in-a-sorted-array/)

## 7. Peak and Mountain Search

**Recognition:** Values rise and then fall, or local slope reveals which side contains a peak.

**Core approach:** Compare `mid` with `mid + 1`; follow the rising slope toward a peak.

- [Find Peak Element](https://leetcode.com/problems/find-peak-element/)
- [Find in Mountain Array](https://leetcode.com/problems/find-in-mountain-array/)

## 8. Rotated Sorted Arrays

**Recognition:** A sorted array was rotated around a pivot.

**Core approach:** At least one side is sorted; decide whether the target lies inside that side. With duplicates, shrink ambiguous boundaries.

- [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
- [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- [Search in Rotated Sorted Array II](https://leetcode.com/problems/search-in-rotated-sorted-array-ii/)

## 9. Flattened Matrix Search

**Recognition:** Matrix rows form one globally sorted sequence.

**Core approach:** Binary-search virtual indices and map index `i` to `matrix[i / cols][i % cols]`.

- [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)

## 10. Restricted-API Binary Search

**Recognition:** Data is hidden behind comparison or cell-access methods, and API calls must be minimized.

**Core approach:** Use monotonic comparisons to eliminate ranges without reading every value.

- [Find the Index of the Large Integer](https://leetcode.com/problems/find-the-index-of-the-large-integer/)
- [Leftmost Column With at Least a One](https://leetcode.com/problems/leftmost-column-with-at-least-a-one/)

## 11. Minimize the Maximum Feasible Answer

**Recognition:** Find the smallest speed, capacity, limit, capability, time, or largest allowed partition sum that makes a task feasible.

**Core approach:** Search `[minimum possible, maximum possible]`; the feasibility predicate changes once from false to true.

- [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)
- [Capacity to Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/)
- [House Robber IV](https://leetcode.com/problems/house-robber-iv/)
- [Minimize the Maximum Difference of Pairs](https://leetcode.com/problems/minimize-the-maximum-difference-of-pairs/)
- [Minimized Maximum of Products Distributed to Any Store](https://leetcode.com/problems/minimized-maximum-of-products-distributed-to-any-store/)
- [Minimum Limit of Balls in a Bag](https://leetcode.com/problems/minimum-limit-of-balls-in-a-bag/)
- [Minimum Time to Repair Cars](https://leetcode.com/problems/minimum-time-to-repair-cars/)
- [Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/)

## 12. Maximize the Minimum Feasible Answer

**Recognition:** Find the largest piece size, minimum sweetness, or per-recipient allocation that remains achievable.

**Core approach:** Search for the last feasible value; feasibility changes once from true to false.

- [Divide Chocolate](https://leetcode.com/problems/divide-chocolate/)
- [Maximum Candies Allocated to K Children](https://leetcode.com/problems/maximum-candies-allocated-to-k-children/)
- [Cutting Ribbons](https://leetcode.com/problems/cutting-ribbons/)

## 13. Real-Valued Binary Search

**Recognition:** Optimize a continuous answer such as an average or distance within a precision tolerance.

**Core approach:** Binary-search doubles for a fixed number of iterations or until the interval is smaller than epsilon.

- [Maximum Average Subarray II](https://leetcode.com/problems/maximum-average-subarray-ii/)
- [Minimize Max Distance to Gas Station](https://leetcode.com/problems/minimize-max-distance-to-gas-station/)

## 14. Binary Search on Removable/Allowed Operations

**Recognition:** Applying the first `k` operations preserves a property only up to some maximum `k`.

**Core approach:** Binary-search `k` and rebuild/check the resulting sequence with a linear predicate.

- [Maximum Number of Removable Characters](https://leetcode.com/problems/maximum-number-of-removable-characters/)

## 15. Per-Query Lower Bound

**Recognition:** For each query, count qualifying sorted values or retrieve the best item under a threshold.

**Core approach:** Sort/preprocess once, then answer every query with lower/upper bound.

- [Successful Pairs of Spells and Potions](https://leetcode.com/problems/successful-pairs-of-spells-and-potions/)
- [Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)
- [Most Beautiful Item for Each Query](https://leetcode.com/problems/most-beautiful-item-for-each-query/)
- [Search Suggestions System](https://leetcode.com/problems/search-suggestions-system/)

## 16. Prefix Sums + Binary Search Sampling

**Recognition:** Random choices must be proportional to weights.

**Core approach:** Build cumulative weights, generate a random target, and lower-bound the first prefix reaching it.

- [Random Pick With Weight](https://leetcode.com/problems/random-pick-with-weight/)

## 17. Count Pairs with Bounds

**Recognition:** Count sorted pairs whose sum lies within a numeric interval.

**Core approach:** For every left index, use lower/upper bound for the valid partner range.

- [Count the Number of Fair Pairs](https://leetcode.com/problems/count-the-number-of-fair-pairs/)

## 18. Prefix/Suffix Validity in an Unsorted Array

**Recognition:** Count values that could be found by binary search even though the whole array is unsorted.

**Core approach:** Precompute prefix maxima and suffix minima; a position is valid when every left value is smaller and every right value is larger.

- [Binary Searchable Numbers in an Unsorted Array](https://leetcode.com/problems/binary-searchable-numbers-in-an-unsorted-array/)

## 19. K-th Value by Counting Smaller Elements

**Recognition:** The answer is the k-th smallest derived value, but explicitly generating all candidates is too expensive.

**Core approach:** Binary-search a candidate value and count how many pairs/products are less than or equal to it.

- [Find K-th Smallest Pair Distance](https://leetcode.com/problems/find-k-th-smallest-pair-distance/)
- [Kth Smallest Product of Two Sorted Arrays](https://leetcode.com/problems/kth-smallest-product-of-two-sorted-arrays/)

## 20. Partition Binary Search Across Two Arrays

**Recognition:** Find the median of two sorted arrays without merging them.

**Core approach:** Binary-search a partition in the smaller array so both left partitions contain exactly half the elements and satisfy cross-boundary ordering.

- [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Find target in sorted data | Exact binary search |
| First value at least target | Lower bound |
| First and last occurrence | Lower + upper bound |
| Integer square/root/count | Numeric answer search |
| Sorted pairs except one value | Parity binary search |
| Array rises then falls | Peak search |
| Sorted array rotated | Sorted-half detection |
| Smallest valid capacity/speed/time | First feasible answer |
| Largest valid allocation/distance | Last feasible answer |
| Continuous optimization | Real-valued binary search |
| Many threshold queries | Preprocess + per-query bound |
| K-th derived pair value | Search value + count predicate |
| Median of two sorted arrays | Partition binary search |

## Recommended Practice Order

1. Binary Search and Search Insert Position
2. First/Last Position
3. Sqrt(x) and Valid Perfect Square
4. Single Element and Find Peak
5. Rotated Array problems
6. Search a 2D Matrix
7. Koko Eating Bananas
8. Shipping Capacity and Split Array Largest Sum
9. Maximize-minimum allocation problems
10. Per-query bounds and weighted random pick
11. Pair-distance/product counting
12. Median of Two Sorted Arrays
