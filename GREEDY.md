# Greedy Problems Segregated by Pattern

Recommended order: **Local greedy → Sorting greedy → Kadane → Jump/reachability → Interval greedy → Frequency greedy → Heap greedy → Constructive greedy**.

> Each problem is placed under the greedy pattern most useful for recognizing its primary solution.

## 1. Cheapest Items and Capacity Filling

**Recognition:** Buy or pack as many items as possible under a budget/capacity.

**Core approach:** Sort ascending and take the cheapest/lightest feasible items first.

- [Buy Two Chocolates](https://leetcode.com/problems/buy-two-chocolates/)
- [How Many Apples Can You Put Into the Basket](https://leetcode.com/problems/how-many-apples-can-you-put-into-the-basket/)

## 2. Greedy Change and Transaction Feasibility

**Recognition:** Each transaction must be completed using resources accumulated earlier.

**Core approach:** Preserve flexible denominations and spend the least useful combination that satisfies the current request.

- [Lemonade Change](https://leetcode.com/problems/lemonade-change/)

## 3. Sort and Pair Corresponding Values

**Recognition:** Minimize total movement by matching two equal-sized sets.

**Core approach:** Sort both arrays and pair elements at equal indices.

- [Minimum Number of Moves to Seat Everyone](https://leetcode.com/problems/minimum-number-of-moves-to-seat-everyone/)

## 4. Construct the Lexicographically Best Arrangement

**Recognition:** Rearrange characters/digits to maximize or minimize lexicographic/numeric value under constraints.

**Core approach:** Place the most valuable feasible symbol first while reserving mandatory positions.

- [Maximum Odd Binary Number](https://leetcode.com/problems/maximum-odd-binary-number/)
- [Construct String With Repeat Limit](https://leetcode.com/problems/construct-string-with-repeat-limit/)
- [Maximum Swap](https://leetcode.com/problems/maximum-swap/)

## 5. Parentheses Balance Bounds

**Recognition:** Parentheses may include flexible/locked positions or only nesting depth is required.

**Core approach:** Track current depth or a range of possible open counts; validity requires the range never to become impossible.

- [Maximum Nesting Depth of the Parentheses](https://leetcode.com/problems/maximum-nesting-depth-of-the-parentheses/)
- [Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/)
- [Check If a Parentheses String Can Be Valid](https://leetcode.com/problems/check-if-a-parentheses-string-can-be-valid/)

## 6. Mismatch Counting and Local String Repair

**Recognition:** A small number of swaps/changes can repair a binary or paired string.

**Core approach:** Count mismatches or inspect independent adjacent pairs instead of searching all edits.

- [Check If One String Swap Can Make Strings Equal](https://leetcode.com/problems/check-if-one-string-swap-can-make-strings-equal/)
- [Minimum Number of Changes to Make Binary String Beautiful](https://leetcode.com/problems/minimum-number-of-changes-to-make-binary-string-beautiful/)

## 7. Greedy Binary Operations

**Recognition:** Flipping at one position deterministically affects a fixed range.

**Core approach:** Scan left to right; when the current effective bit is wrong, the next flip is forced.

- [Minimum Operations to Make Binary Array Elements Equal to One I](https://leetcode.com/problems/minimum-operations-to-make-binary-array-elements-equal-to-one-i/)
- [Minimum Number of K Consecutive Bit Flips](https://leetcode.com/problems/minimum-number-of-k-consecutive-bit-flips/)

## 8. Suffix Maximum and Visibility

**Recognition:** An item qualifies only if every item to its right is smaller.

**Core approach:** Scan from right to left while maintaining the suffix maximum.

- [Buildings With an Ocean View](https://leetcode.com/problems/buildings-with-an-ocean-view/)

## 9. Frequency and Parity Greedy

**Recognition:** Character frequencies must meet parity, uniqueness, or keyboard-placement constraints.

**Core approach:** Sort/count frequencies and spend deletions or prime positions on the most valuable counts.

- [Minimum Length of String After Operations](https://leetcode.com/problems/minimum-length-of-string-after-operations/)
- [Construct K Palindrome Strings](https://leetcode.com/problems/construct-k-palindrome-strings/)
- [Minimum Number of Pushes to Type Word II](https://leetcode.com/problems/minimum-number-of-pushes-to-type-word-ii/)
- [Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/)

## 10. Inversion Counting by Movement

**Recognition:** Separate two symbol types using adjacent swaps.

**Core approach:** Scan once and accumulate how many opposite-type symbols each current symbol must cross.

- [Separate Black and White Balls](https://leetcode.com/problems/separate-black-and-white-balls/)

## 11. Sort and Enforce Increasing Uniqueness

**Recognition:** Values must become unique or obey a bounded step relationship.

**Core approach:** Sort and raise each value only to the smallest valid value above its predecessor.

- [Minimum Increment to Make Array Unique](https://leetcode.com/problems/minimum-increment-to-make-array-unique/)
- [Maximum Element After Decreasing and Rearranging](https://leetcode.com/problems/maximum-element-after-decreasing-and-rearranging/)

## 12. Kadane's Algorithm Family

**Recognition:** Find the best contiguous sum, absolute sum, or circular sum.

**Core approach:** Maintain best/worst subarray ending at each position; circular maximum uses total sum minus minimum subarray.

- [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- [Maximum Absolute Sum of Any Subarray](https://leetcode.com/problems/maximum-absolute-sum-of-any-subarray/)
- [Maximum Sum Circular Subarray](https://leetcode.com/problems/maximum-sum-circular-subarray/)

## 13. Circular and Complementary Window

**Recognition:** Select/remove a fixed number of elements from circular positions or both ends.

**Core approach:** Convert the choice to a fixed-size circular window or the complement of a middle window.

- [Minimum Swaps to Group All 1's Together II](https://leetcode.com/problems/minimum-swaps-to-group-all-1s-together-ii/)
- [Maximum Points You Can Obtain From Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)

## 14. Alternating Trend Scan

**Recognition:** Adjacent comparisons must alternate between greater and smaller.

**Core approach:** Track the current run and reset when the comparison repeats or becomes equal.

- [Longest Turbulent Subarray](https://leetcode.com/problems/longest-turbulent-subarray/)

## 15. Jump and Reachability Greedy

**Recognition:** Each index extends the reachable frontier.

**Core approach:** Track farthest reach; for minimum jumps, process one BFS-like reachable layer at a time.

- [Jump Game](https://leetcode.com/problems/jump-game/)
- [Jump Game II](https://leetcode.com/problems/jump-game-ii/)
- [Jump Game VII](https://leetcode.com/problems/jump-game-vii/)

## 16. Reset-on-Deficit Greedy

**Recognition:** Find a circular starting point that can sustain a running resource balance.

**Core approach:** If the running balance becomes negative, no earlier point in that failed segment can be the answer.

- [Gas Station](https://leetcode.com/problems/gas-station/)

## 17. Consecutive-Group Construction

**Recognition:** Values must be partitioned into consecutive groups of fixed length.

**Core approach:** Always start with the smallest remaining value and consume the full consecutive sequence.

- [Hand of Straights](https://leetcode.com/problems/hand-of-straights/)

## 18. Prefix-Average Feasibility

**Recognition:** Redistribute excess leftward/rightward to minimize the maximum array value.

**Core approach:** The answer is the maximum ceiling of every prefix average.

- [Minimize Maximum of Array](https://leetcode.com/problems/minimize-maximum-of-array/)

## 19. Sort and Keep Best per Category

**Recognition:** Select high-value items with distinct category keys.

**Core approach:** Retain the maximum candidate per key, then choose the globally best required categories.

- [Maximize Y-Sum by Picking a Triplet of Distinct X-Values](https://leetcode.com/problems/maximize-ysum-by-picking-a-triplet-of-distinct-xvalues/)

## 20. Remove a Constant Number of Extremes

**Recognition:** A small fixed number of edits can eliminate extreme values.

**Core approach:** Sort and enumerate how many removals come from each end.

- [Minimum Difference Between Largest and Smallest Value in Three Moves](https://leetcode.com/problems/minimum-difference-between-largest-and-smallest-value-in-three-moves/)

## 21. Degree-Based Greedy Assignment

**Recognition:** Assign larger labels to higher-impact graph nodes.

**Core approach:** Sort nodes by degree and assign the largest values to the largest degrees.

- [Maximum Total Importance of Roads](https://leetcode.com/problems/maximum-total-importance-of-roads/)

## 22. Queue and Cyclic Simulation

**Recognition:** Competing groups repeatedly act in cyclic order.

**Core approach:** Store each group's active indices in queues and schedule the winner into the next round.

- [Dota2 Senate](https://leetcode.com/problems/dota2-senate/)

## 23. Componentwise Target Feasibility

**Recognition:** Several candidates can be merged only if none exceeds the target in any dimension.

**Core approach:** Keep compatible candidates and mark which target dimensions they satisfy.

- [Merge Triplets to Form Target Triplet](https://leetcode.com/problems/merge-triplets-to-form-target-triplet/)

## 24. Last-Occurrence Partitioning

**Recognition:** Split a string so each character appears in only one segment.

**Core approach:** Track each character's last index and close a segment when the current position reaches the farthest required end.

- [Partition Labels](https://leetcode.com/problems/partition-labels/)

## 25. Sort by Deadline or Arrival

**Recognition:** Complete the maximum number of tasks before their deadlines or assign entities by cost difference.

**Core approach:** Sort by the decisive time/cost key and make the locally forced choice.

- [Eliminate Maximum Number of Monsters](https://leetcode.com/problems/eliminate-maximum-number-of-monsters/)
- [Two City Scheduling](https://leetcode.com/problems/two-city-scheduling/)

## 26. Interval Scheduling

**Recognition:** Select the maximum number of non-overlapping pairs/intervals.

**Core approach:** Sort by end time and repeatedly take the earliest finishing compatible interval.

- [Maximum Length of Pair Chain](https://leetcode.com/problems/maximum-length-of-pair-chain/)

## 27. Best Pair with Running State

**Recognition:** A pair score separates into a left contribution and a right contribution.

**Core approach:** Maintain the best left-side contribution seen before evaluating each right endpoint.

- [Best Sightseeing Pair](https://leetcode.com/problems/best-sightseeing-pair/)

## 28. Sort-Connected Components

**Recognition:** Swaps are allowed among values connected by a threshold relation.

**Core approach:** Sort values into connected groups and assign each group's smallest values to its smallest indices.

- [Make Lexicographically Smallest Array by Swapping Elements](https://leetcode.com/problems/make-lexicographically-smallest-array-by-swapping-elements/)

## 29. Balanced String Deletions

**Recognition:** Delete the fewest characters so all characters of one type precede another.

**Core approach:** Track deletions for the prefix versus deleting the current misplaced character.

- [Minimum Deletions to Make String Balanced](https://leetcode.com/problems/minimum-deletions-to-make-string-balanced/)

## 30. Two-Pass Local Constraints

**Recognition:** Each position must exceed neighbors based on directional comparisons.

**Core approach:** Satisfy left constraints in one pass and right constraints in another, then take the maximum requirement.

- [Candy](https://leetcode.com/problems/candy/)

## 31. Run-Based Game Counting

**Recognition:** Moves depend only on lengths of consecutive equal-character runs.

**Core approach:** Count playable positions contributed by each run and compare players' totals.

- [Remove Colored Pieces If Both Neighbors Are the Same Color](https://leetcode.com/problems/remove-colored-pieces-if-both-neighbors-are-the-same-color/)

## 32. Order High-Value String Removals

**Recognition:** Two overlapping substring-removal operations have different rewards.

**Core approach:** Remove the higher-value pattern first using a stack, then process the other.

- [Maximum Score From Removing Substrings](https://leetcode.com/problems/maximum-score-from-removing-substrings/)

## 33. Adjacent-Row Aggregation

**Recognition:** The result accumulates from consecutive nonempty rows.

**Core approach:** Track the previous row's count and add its product with the current row.

- [Number of Laser Beams in a Bank](https://leetcode.com/problems/number-of-laser-beams-in-a-bank/)

## 34. Reverse-Process Construction

**Recognition:** Reproduce a desired reveal/removal order.

**Core approach:** Simulate the operations backward with a deque.

- [Reveal Cards in Increasing Order](https://leetcode.com/problems/reveal-cards-in-increasing-order/)

## 35. Matrix Greedy Construction and Flipping

**Recognition:** Build or flip matrix values to satisfy row/column totals or maximize score.

**Core approach:** Make locally dominant row/column choices and preserve global sum invariants.

- [Find Valid Matrix Given Row and Column Sums](https://leetcode.com/problems/find-valid-matrix-given-row-and-column-sums/)
- [Score After Flipping Matrix](https://leetcode.com/problems/score-after-flipping-matrix/)
- [Flip Columns for Maximum Number of Equal Rows](https://leetcode.com/problems/flip-columns-for-maximum-number-of-equal-rows/)
- [Maximum Matrix Sum](https://leetcode.com/problems/maximum-matrix-sum/)

## 36. Multiset Equivalence

**Recognition:** Arbitrary subarray reversals effectively allow any permutation.

**Core approach:** Compare value frequencies in both arrays.

- [Make Two Arrays Equal by Reversing Subarrays](https://leetcode.com/problems/make-two-arrays-equal-by-reversing-subarrays/)

## 37. Sorted Prefix/Suffix Repair

**Recognition:** Remove one middle segment so the remaining prefix and suffix form a sorted array.

**Core approach:** Find maximal sorted prefix/suffix, then merge them with two pointers.

- [Shortest Subarray to Be Removed to Make Array Sorted](https://leetcode.com/problems/shortest-subarray-to-be-removed-to-make-array-sorted/)

## 38. Partition into Independently Sortable Chunks

**Recognition:** Sorting individual segments must produce the globally sorted array.

**Core approach:** Close a chunk when its prefix maximum matches the value/index condition of the sorted prefix.

- [Max Chunks to Make Sorted](https://leetcode.com/problems/max-chunks-to-make-sorted/)

## 39. Next Lexicographical Arrangement

**Recognition:** Produce the immediately next permutation.

**Core approach:** Find the rightmost ascent, swap its pivot with the smallest larger suffix value, then reverse the suffix.

- [Next Permutation](https://leetcode.com/problems/next-permutation/)

## 40. Repeated Maximum Extraction

**Recognition:** Repeatedly take and transform the current maximum value.

**Core approach:** Use a max-heap.

- [Maximal Score After Applying K Operations](https://leetcode.com/problems/maximal-score-after-applying-k-operations/)

## 41. Gain/Loss Transformation

**Recognition:** One subarray operation changes frequencies or values, and the best interval gain must be found.

**Core approach:** Convert each candidate operation into a gain array and apply Kadane-style optimization.

- [Maximum Frequency After Subarray Operation](https://leetcode.com/problems/maximum-frequency-after-subarray-operation/)

## 42. Constrained Packing after Sorting

**Recognition:** Items enter through changing capacity constraints.

**Core approach:** Reduce capacities to effective prefix minima, then greedily fit sorted items.

- [Put Boxes Into the Warehouse I](https://leetcode.com/problems/put-boxes-into-the-warehouse-i/)

## 43. Boundary-Contribution Sorting

**Recognition:** Partition scores differ only by which adjacent pairs become boundaries.

**Core approach:** Sort adjacent-pair contributions and compare the largest versus smallest required selections.

- [Put Marbles in Bags](https://leetcode.com/problems/put-marbles-in-bags/)

## 44. Expand from a Required Index

**Recognition:** Find the best subarray containing a mandatory index, with score based on its minimum and length.

**Core approach:** Expand toward the larger neighboring value while tracking the running minimum.

- [Maximum Score of a Good Subarray](https://leetcode.com/problems/maximum-score-of-a-good-subarray/)

## 45. Parity Gain on Tree/Array Values

**Recognition:** Operations toggle pairs, so only an even number of choices may be changed.

**Core approach:** Sum every positive gain, then repair parity by sacrificing the smallest absolute gain if necessary.

- [Find the Maximum Sum of Node Values](https://leetcode.com/problems/find-the-maximum-sum-of-node-values/)

## 46. Count Required Upward Transitions

**Recognition:** Range-increment operations construct a target array from zero.

**Core approach:** Pay for the first height and every positive rise from the previous value.

- [Minimum Number of Increments on Subarrays to Form a Target Array](https://leetcode.com/problems/minimum-number-of-increments-on-subarrays-to-form-a-target-array/)

## 47. Prime-Score Greedy Selection

**Recognition:** Values have multiplicative scores and can be selected a limited number of times based on dominance ranges.

**Core approach:** Compute each value's usable count with monotonic boundaries, then consume choices in descending value order.

- [Apply Operations to Maximize Score](https://leetcode.com/problems/apply-operations-to-maximize-score/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Buy/pack under a limit | Sort ascending |
| Change must be made online | Preserve flexible resources |
| Best contiguous sum | Kadane |
| Farthest reachable index | Frontier greedy |
| Circular resource balance | Reset on deficit |
| Maximum non-overlapping pairs | Sort by end |
| Flexible parentheses | Min/max open bounds |
| Character frequency constraints | Count + greedy placement |
| Fixed range flips | Left-to-right forced flips |
| Repeated current maximum | Max-heap |
| Build target with range increments | Positive differences |
| Matrix sign/flip optimization | Global parity invariant |

## Recommended Practice Order

1. Buy Two Chocolates and Lemonade Change
2. Jump Game I and II
3. Gas Station
4. Kadane family
5. Partition Labels
6. Valid Parenthesis String
7. Interval and deadline scheduling
8. Candy and frequency greedy
9. Matrix greedy problems
10. Constructive ordering problems
11. Heap and gain-transformation greedy
