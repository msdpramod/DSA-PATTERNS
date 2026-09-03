# 175 Arrays, Strings, Hashing, Prefix Sum, Sorting, and Design Problems by Pattern

Recommended order: **Linear scan → Frequency map → Hashing → Subsequence → Prefix sum → In-place marking → Matrix simulation → Design problems**.

> Some problems fit multiple categories. Each appears under the pattern most useful for recognizing its primary solution.

## 1. Direct Array/String Construction

**Recognition:** Produce an output through a straightforward pass without complex state.

**Core approach:** Scan once, append or calculate locally, and avoid unnecessary auxiliary structures.

- [Concatenation of Array](https://leetcode.com/problems/concatenation-of-array/)
- [Score of a String](https://leetcode.com/problems/score-of-a-string/)
- [Length of Last Word](https://leetcode.com/problems/length-of-last-word/)
- [Number of Senior Citizens](https://leetcode.com/problems/number-of-senior-citizens/)
- [Max Consecutive Ones](https://leetcode.com/problems/max-consecutive-ones/)
- [Largest 3-Same-Digit Number in String](https://leetcode.com/problems/largest-3-same-digit-number-in-string/)
- [Circular Sentence](https://leetcode.com/problems/circular-sentence/)

## 2. Right-to-Left Suffix State

**Recognition:** Each position depends on the best value strictly to its right.

**Core approach:** Scan backward while maintaining the suffix maximum or another suffix aggregate.

- [Replace Elements With Greatest Element on Right Side](https://leetcode.com/problems/replace-elements-with-greatest-element-on-right-side/)

## 3. Subsequence Matching

**Recognition:** Determine whether one string can be formed by deleting characters from another, or how many source passes are needed.

**Core approach:** Advance the target pointer only on a match; restart or preprocess next positions for repeated source scans.

- [Is Subsequence](https://leetcode.com/problems/is-subsequence/)
- [Append Characters to String to Make Subsequence](https://leetcode.com/problems/append-characters-to-string-to-make-subsequence/)
- [Shortest Way to Form String](https://leetcode.com/problems/shortest-way-to-form-string/)

## 4. Frequency Map — Equality and Permutation

**Recognition:** Order is irrelevant; only occurrence counts determine equivalence or feasibility.

**Core approach:** Count each value/character and compare frequency profiles.

- [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
- [Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- [Palindrome Permutation](https://leetcode.com/problems/palindrome-permutation/)
- [Group Anagrams](https://leetcode.com/problems/group-anagrams/)

## 5. Bijection and Relationship Mapping

**Recognition:** Elements or words from one domain must map consistently—and sometimes uniquely—to another.

**Core approach:** Use forward and reverse maps when one-to-one correspondence is required.

- [Find Anagram Mappings](https://leetcode.com/problems/find-anagram-mappings/)
- [Sentence Similarity](https://leetcode.com/problems/sentence-similarity/)
- [Isomorphic Strings](https://leetcode.com/problems/isomorphic-strings/)
- [Word Pattern](https://leetcode.com/problems/word-pattern/)

## 6. Frequency-Based Selection

**Recognition:** Select values based on uniqueness, majority, rank among distinct values, or a relation between value and frequency.

**Core approach:** Build frequencies first, then scan in the output's required order.

- [Largest Unique Number](https://leetcode.com/problems/largest-unique-number/)
- [Majority Element](https://leetcode.com/problems/majority-element/)
- [Maximum Difference Between Even and Odd Frequency I](https://leetcode.com/problems/maximum-difference-between-even-and-odd-frequency-i/)
- [Kth Distinct String in an Array](https://leetcode.com/problems/kth-distinct-string-in-an-array/)
- [Find Lucky Integer in an Array](https://leetcode.com/problems/find-lucky-integer-in-an-array/)

## 7. Hashing for Pair and Neighbor Counts

**Recognition:** Count or find values whose complement, successor, or duplicate was already seen.

**Core approach:** Store seen values/frequencies and update the answer using the needed counterpart.

- [Two Sum](https://leetcode.com/problems/two-sum/)
- [Counting Elements](https://leetcode.com/problems/counting-elements/)
- [Divide Array Into Equal Pairs](https://leetcode.com/problems/divide-array-into-equal-pairs/)
- [Number of Good Pairs](https://leetcode.com/problems/number-of-good-pairs/)

## 8. Character Inventory

**Recognition:** Determine how many words/copies can be built from available characters.

**Core approach:** Compare required frequency vectors against the available inventory.

- [Maximum Number of Balloons](https://leetcode.com/problems/maximum-number-of-balloons/)
- [Find Words That Can Be Formed by Characters](https://leetcode.com/problems/find-words-that-can-be-formed-by-characters/)
- [Count the Number of Consistent Strings](https://leetcode.com/problems/count-the-number-of-consistent-strings/)
- [Ransom Note](https://leetcode.com/problems/ransom-note/)

## 9. Canonicalization and Grouping

**Recognition:** Different raw strings should be considered equivalent after normalization.

**Core approach:** Convert each item into a canonical key, then deduplicate or group by that key.

- [Unique Email Addresses](https://leetcode.com/problems/unique-email-addresses/)
- [Group Shifted Strings](https://leetcode.com/problems/group-shifted-strings/)

## 10. Position Map and Modular Shift

**Recognition:** Repeated lookups of positions or many shift operations can be collapsed.

**Core approach:** Precompute position indices or combine all shifts into one net modular displacement.

- [Single-Row Keyboard](https://leetcode.com/problems/single-row-keyboard/)
- [Perform String Shifts](https://leetcode.com/problems/perform-string-shifts/)

## 11. String Comparison and Search

**Recognition:** Compare common prefixes or detect whether one string occurs inside another.

**Core approach:** Scan aligned positions for a prefix; use direct matching or a string-search algorithm for containment.

- [Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
- [String Matching in an Array](https://leetcode.com/problems/string-matching-in-an-array/)

## 12. Stream and Iterator Design

**Recognition:** Values arrive incrementally and queries must reflect current state without recomputing everything.

**Core approach:** Retain only the state required by future operations using queues, maps, counters, or iterator cursors.

- [Design Compressed String Iterator](https://leetcode.com/problems/design-compressed-string-iterator/)
- [Logger Rate Limiter](https://leetcode.com/problems/logger-rate-limiter/)
- [Moving Average From Data Stream](https://leetcode.com/problems/moving-average-from-data-stream/)
- [First Unique Number](https://leetcode.com/problems/first-unique-number/)
- [Zigzag Iterator](https://leetcode.com/problems/zigzag-iterator/)
- [Design a Leaderboard](https://leetcode.com/problems/design-a-leaderboard/)

## 13. Matrix Validation and Frequency Aggregation

**Recognition:** Validate row/column symmetry or find values satisfying cross-row/cross-column frequency constraints.

**Core approach:** Count by row and column or compare mirrored coordinates directly.

- [Valid Word Square](https://leetcode.com/problems/valid-word-square/)
- [Lonely Pixel I](https://leetcode.com/problems/lonely-pixel-i/)
- [Find Smallest Common Element in All Rows](https://leetcode.com/problems/find-smallest-common-element-in-all-rows/)

## 14. Sparse Matrix Computation

**Recognition:** Most matrix entries are zero, so dense multiplication wastes work.

**Core approach:** Store/process only nonzero coordinates and multiply compatible sparse entries.

- [Sparse Matrix Multiplication](https://leetcode.com/problems/sparse-matrix-multiplication/)

## 15. Grid and Game Simulation

**Recognition:** Apply rules repeatedly to a board or maintain game state after each move.

**Core approach:** Separate detection from mutation when updates are simultaneous; maintain compact row/column state when possible.

- [Candy Crush](https://leetcode.com/problems/candy-crush/)
- [Design Tic-Tac-Toe](https://leetcode.com/problems/design-tic-tac-toe/)
- [Design Snake Game](https://leetcode.com/problems/design-snake-game/)

## 16. One-Edit Comparison

**Recognition:** Two strings may differ by exactly one insertion, deletion, or replacement.

**Core approach:** Align pointers; at the first mismatch, advance according to the length difference.

- [One Edit Distance](https://leetcode.com/problems/one-edit-distance/)

## 17. In-Place Word Reversal

**Recognition:** Reverse word order inside a mutable character array.

**Core approach:** Reverse the whole array, then reverse each individual word.

- [Reverse Words in a String II](https://leetcode.com/problems/reverse-words-in-a-string-ii/)

## 18. Cross-Array Extrema

**Recognition:** Select values from different sorted arrays to maximize distance.

**Core approach:** Maintain global minimum/maximum from prior arrays and combine them with the current array's endpoints.

- [Maximum Distance in Arrays](https://leetcode.com/problems/maximum-distance-in-arrays/)

## 19. Prefix Sum

**Recognition:** Query range sums or compare left and right cumulative totals.

**Core approach:** Precompute cumulative sums so each range or split calculation is constant time.

- [Find Pivot Index](https://leetcode.com/problems/find-pivot-index/)
- [Range Sum Query — Immutable](https://leetcode.com/problems/range-sum-query-immutable/)
- [Maximum Score After Splitting a String](https://leetcode.com/problems/maximum-score-after-splitting-a-string/)

## 20. In-Place Filtering

**Recognition:** Remove matching elements from an array without allocating another output array.

**Core approach:** Use a write pointer for retained elements.

- [Remove Element](https://leetcode.com/problems/remove-element/)

## 21. Cyclic Index Marking

**Recognition:** Values lie in a bounded range related to array length, and missing/repeated values must be found in constant extra space.

**Core approach:** Use sign marking, cyclic placement, or arithmetic counts at value-derived indices.

- [Find All Numbers Disappeared in an Array](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
- [Find Missing and Repeated Values](https://leetcode.com/problems/find-missing-and-repeated-values/)

## 22. Hash Table Implementation

**Recognition:** Implement set/map operations without using the built-in hash structure.

**Core approach:** Use bucket arrays with chaining or open addressing and a stable hash-to-bucket mapping.

- [Design HashSet](https://leetcode.com/problems/design-hashset/)
- [Design HashMap](https://leetcode.com/problems/design-hashmap/)

## 23. Sorting and Reference Comparison

**Recognition:** Count positions differing from their sorted order.

**Core approach:** Sort a copy or use counting sort when the value range is small.

- [Height Checker](https://leetcode.com/problems/height-checker/)

## 24. Array Trend and Local Invariants

**Recognition:** Validate parity alternation, monotonicity, one rotation break, or the longest directional run.

**Core approach:** Scan adjacent pairs and maintain a violation or current-run counter.

- [Special Array I](https://leetcode.com/problems/special-array-i/)
- [Check If Array Is Sorted and Rotated](https://leetcode.com/problems/check-if-array-is-sorted-and-rotated/)
- [Monotonic Array](https://leetcode.com/problems/monotonic-array/)
- [Longest Strictly Increasing or Strictly Decreasing Subarray](https://leetcode.com/problems/longest-strictly-increasing-or-strictly-decreasing-subarray/)
- [Maximum Ascending Subarray Sum](https://leetcode.com/problems/maximum-ascending-subarray-sum/)

## 25. Local Greedy Placement

**Recognition:** Place items in a binary layout while respecting adjacent spacing.

**Core approach:** Scan and place whenever both neighbors are empty, updating the array immediately.

- [Can Place Flowers](https://leetcode.com/problems/can-place-flowers/)

## 26. Pascal Recurrence

**Recognition:** Construct binomial coefficients row by row.

**Core approach:** Each inner value is the sum of two values from the previous row; update backward for one-row space.

- [Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/)
- [Pascal's Triangle II](https://leetcode.com/problems/pascals-triangle-ii/)

## 27. Monotonic Stack Lookup

**Recognition:** Find the first greater value to the right for selected values.

**Core approach:** Process the reference array with a decreasing stack and map each popped value to its next greater value.

- [Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/)

## 28. Set Difference to Find a Terminal Node

**Recognition:** Directed pairs form a path and one destination has no outgoing edge.

**Core approach:** Store every source and return the destination absent from the source set.

- [Destination City](https://leetcode.com/problems/destination-city/)

## 29. Track Extreme Values

**Recognition:** The result depends only on the two smallest and two largest values.

**Core approach:** Sort or track four extrema in one pass.

- [Maximum Product Difference Between Two Pairs](https://leetcode.com/problems/maximum-product-difference-between-two-pairs/)

## 30. Digit Rotation Mapping

**Recognition:** Rotate digits by 180 degrees and determine whether the resulting number is valid and different.

**Core approach:** Map rotatable digits while scanning from the ends and reject invalid digits.

- [Confusing Number](https://leetcode.com/problems/confusing-number/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Simple output from each element | Direct scan |
| Depends on values to the right | Backward suffix state |
| Delete characters to form target | Subsequence pointers |
| Order irrelevant, counts matter | Frequency map |
| One-to-one symbol relationship | Two-way mapping |
| Normalize before comparing | Canonical key |
| Values arrive incrementally | Stream state |
| Many range/split sums | Prefix sum |
| Values lie in 1…n | Index marking |
| Adjacent trend constraints | Local invariant scan |
| First greater value to right | Monotonic stack |
| Implement O(1)-average lookup | Hash buckets |

## Recommended Practice Order

1. Direct array and string scans
2. Contains Duplicate and Valid Anagram
3. Two Sum and frequency counting
4. Is Subsequence
5. Group Anagrams and mapping problems
6. Prefix-sum problems
7. In-place filtering and index marking
8. Matrix and simulation problems
9. Stream/iterator design
10. HashSet and HashMap implementation

# Additional Pattern Set

## 31. Direct Simulation and State Tracking

**Recognition:** Follow the stated process while retaining only the state needed for the next step.

**Core approach:** Translate rules directly, separating simultaneous reads from writes where necessary.

- [Path Crossing](https://leetcode.com/problems/path-crossing/)
- [Minimum Changes to Make Alternating Binary String](https://leetcode.com/problems/minimum-changes-to-make-alternating-binary-string/)
- [Number of Students Unable to Eat Lunch](https://leetcode.com/problems/number-of-students-unable-to-eat-lunch/)
- [Time Needed to Buy Tickets](https://leetcode.com/problems/time-needed-to-buy-tickets/)
- [Array Transformation](https://leetcode.com/problems/array-transformation/)
- [Average Waiting Time](https://leetcode.com/problems/average-waiting-time/)
- [Push Dominoes](https://leetcode.com/problems/push-dominoes/)
- [Sign of the Product of an Array](https://leetcode.com/problems/sign-of-the-product-of-an-array/)
- [Number of Zero-Filled Subarrays](https://leetcode.com/problems/number-of-zero-filled-subarrays/)
- [Sequential Digits](https://leetcode.com/problems/sequential-digits/)
- [Champagne Tower](https://leetcode.com/problems/champagne-tower/)
- [Time Taken to Cross the Door](https://leetcode.com/problems/time-taken-to-cross-the-door/)

## 32. Frequency Maps and Character Inventories

**Recognition:** Counts—not positions—determine whether strings can be built, balanced, or compared.

**Core approach:** Build frequency vectors and derive feasibility or maximum construction counts.

- [Redistribute Characters to Make All Strings Equal](https://leetcode.com/problems/redistribute-characters-to-make-all-strings-equal/)
- [Longest Palindrome](https://leetcode.com/problems/longest-palindrome/)
- [First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
- [Largest Substring Between Two Equal Characters](https://leetcode.com/problems/largest-substring-between-two-equal-characters/)
- [Find Common Characters](https://leetcode.com/problems/find-common-characters/)
- [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- [Sort Characters by Frequency](https://leetcode.com/problems/sort-characters-by-frequency/)
- [Word Subsets](https://leetcode.com/problems/word-subsets/)
- [Uncommon Words From Two Sentences](https://leetcode.com/problems/uncommon-words-from-two-sentences/)

## 33. Hash Sets, Intersections, and Consecutive Values

**Recognition:** Fast membership tests reveal intersections, missing relations, or sequence starts.

**Core approach:** Store values in a set and process only canonical candidates.

- [Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/)
- [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- [Find the Difference of Two Arrays](https://leetcode.com/problems/find-the-difference-of-two-arrays/)
- [Check If a String Contains All Binary Codes of Size K](https://leetcode.com/problems/check-if-a-string-contains-all-binary-codes-of-size-k/)

## 34. Missing, Repeated, and Indexed Values

**Recognition:** Values occupy a bounded domain tied to array length.

**Core approach:** Use frequency counting, sign marking, XOR, or cyclic placement.

- [Set Mismatch](https://leetcode.com/problems/set-mismatch/)
- [Find All Duplicates in an Array](https://leetcode.com/problems/find-all-duplicates-in-an-array/)
- [First Missing Positive](https://leetcode.com/problems/first-missing-positive/)
- [Convert an Array Into a 2D Array With Conditions](https://leetcode.com/problems/convert-an-array-into-a-2d-array-with-conditions/)

## 35. Prefix Sums and Prefix Counts

**Recognition:** Many ranges, splits, or subarrays depend on cumulative values.

**Core approach:** Store prefix totals or prefix-state frequencies and convert each range to a difference.

- [Count Vowel Strings in Ranges](https://leetcode.com/problems/count-vowel-strings-in-ranges/)
- [Range Sum Query 2D — Immutable](https://leetcode.com/problems/range-sum-query-2d-immutable/)
- [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- [Minimum Number of Operations to Move All Balls to Each Box](https://leetcode.com/problems/minimum-number-of-operations-to-move-all-balls-to-each-box/)
- [Number of Ways to Split Array](https://leetcode.com/problems/number-of-ways-to-split-array/)
- [Minimum Penalty for a Shop](https://leetcode.com/problems/minimum-penalty-for-a-shop/)
- [Sum of Absolute Differences in a Sorted Array](https://leetcode.com/problems/sum-of-absolute-differences-in-a-sorted-array/)
- [Contiguous Array](https://leetcode.com/problems/contiguous-array/)

## 36. Prefix Sum + Hash Map for Subarray Counts

**Recognition:** Count subarrays whose sum, remainder, or parity matches a target.

**Core approach:** Store how often each required earlier prefix state has occurred.

- [Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- [Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- [Make Sum Divisible by P](https://leetcode.com/problems/make-sum-divisible-by-p/)
- [Number of Sub-arrays With Odd Sum](https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/)
- [Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
- [Number of Submatrices That Sum to Target](https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/)

## 37. Difference Arrays and Range Updates

**Recognition:** Many interval additions or shifts affect ranges.

**Core approach:** Record changes at boundaries, then recover values with a prefix accumulation.

- [Shifting Letters II](https://leetcode.com/problems/shifting-letters-ii/)
- [Brightest Position on Street](https://leetcode.com/problems/brightest-position-on-street/)

## 38. Sorting Fundamentals and Custom Ordering

**Recognition:** Reordering reveals structure or the comparator defines the result.

**Core approach:** Select comparison, counting, bucket, merge, or quick sort according to constraints.

- [Sort an Array](https://leetcode.com/problems/sort-an-array/)
- [Sort Colors](https://leetcode.com/problems/sort-colors/)
- [Relative Sort Array](https://leetcode.com/problems/relative-sort-array/)
- [Sort the People](https://leetcode.com/problems/sort-the-people/)
- [Sort Array by Increasing Frequency](https://leetcode.com/problems/sort-array-by-increasing-frequency/)
- [Custom Sort String](https://leetcode.com/problems/custom-sort-string/)
- [Wiggle Sort](https://leetcode.com/problems/wiggle-sort/)
- [Largest Number](https://leetcode.com/problems/largest-number/)
- [Sort the Jumbled Numbers](https://leetcode.com/problems/sort-the-jumbled-numbers/)
- [Divide Array Into Arrays With Max Difference](https://leetcode.com/problems/divide-array-into-arrays-with-max-difference/)

## 39. Greedy Array Decisions

**Recognition:** A locally optimal action can be proven never to harm future choices.

**Core approach:** Sort or scan while maintaining the invariant that the current prefix is optimal.

- [Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/)
- [Non-Decreasing Array](https://leetcode.com/problems/non-decreasing-array/)
- [Minimum Number of Operations to Make Array Empty](https://leetcode.com/problems/minimum-number-of-operations-to-make-array-empty/)
- [Find Polygon With the Largest Perimeter](https://leetcode.com/problems/find-polygon-with-the-largest-perimeter/)

## 40. Majority and Dominant Elements

**Recognition:** A value occurs more than a fixed fraction of the array or must dominate both sides of a split.

**Core approach:** Use Boyer–Moore candidate elimination, then verify counts.

- [Majority Element II](https://leetcode.com/problems/majority-element-ii/)
- [Minimum Index of a Valid Split](https://leetcode.com/problems/minimum-index-of-a-valid-split/)
- [Special Array With X Elements Greater Than or Equal to X](https://leetcode.com/problems/special-array-with-x-elements-greater-than-or-equal-x/)

## 41. String Encoding, Parsing, and Substitution

**Recognition:** Strings require unambiguous framing, recursive replacement, or exact formatting.

**Core approach:** Encode lengths/delimiters explicitly or parse using a controlled cursor and dependency expansion.

- [Encode and Decode Strings](https://leetcode.com/problems/encode-and-decode-strings/)
- [Apply Substitutions](https://leetcode.com/problems/apply-substitutions/)
- [Text Justification](https://leetcode.com/problems/text-justification/)

## 42. String Windows, Search, and Partition

**Recognition:** Find repeated patterns, anagrams, substrings, or the fewest unique-character segments.

**Core approach:** Use sliding-window counts, KMP/rolling hash, or greedy restart on repetition.

- [Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- [Find the Index of the First Occurrence in a String](https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/)
- [Repeated DNA Sequences](https://leetcode.com/problems/repeated-dna-sequences/)
- [Optimal Partition of String](https://leetcode.com/problems/optimal-partition-of-string/)
- [Shortest Palindrome](https://leetcode.com/problems/shortest-palindrome/)
- [Find the Length of the Longest Common Prefix](https://leetcode.com/problems/find-the-length-of-the-longest-common-prefix/)

## 43. Palindromes and Balanced Strings

**Recognition:** Count or construct palindromic subsequences, or repair an imbalanced bracket string.

**Core approach:** Exploit outer-character positions, enumerate masks when small, or track unmatched brackets.

- [Unique Length-3 Palindromic Subsequences](https://leetcode.com/problems/unique-length-3-palindromic-subsequences/)
- [Maximum Product of the Length of Two Palindromic Subsequences](https://leetcode.com/problems/maximum-product-of-the-length-of-two-palindromic-subsequences/)
- [Minimum Number of Swaps to Make the String Balanced](https://leetcode.com/problems/minimum-number-of-swaps-to-make-the-string-balanced/)
- [Minimum Remove to Make Valid Parentheses](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/)

## 44. Grid and Matrix Processing

**Recognition:** Validate, simulate visibility, or optimize movement across a matrix.

**Core approach:** Track row/column state, traverse directional rays, or reduce the grid to prefix summaries.

- [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/)
- [Grid Game](https://leetcode.com/problems/grid-game/)
- [Count Unguarded Cells in the Grid](https://leetcode.com/problems/count-unguarded-cells-in-the-grid/)
- [Brick Wall](https://leetcode.com/problems/brick-wall/)

## 45. Sparse Structures

**Recognition:** Most entries are zero, so dense iteration is wasteful.

**Core approach:** Store only nonzero index-value pairs and intersect compatible indices.

- [Dot Product of Two Sparse Vectors](https://leetcode.com/problems/dot-product-of-two-sparse-vectors/)

## 46. Ratios and Combinatorial Pair Counting

**Recognition:** Pairs are equal under a normalized key or can be counted as total minus invalid pairs.

**Core approach:** Normalize with GCD or derive an invariant key, then count earlier matches.

- [Number of Pairs of Interchangeable Rectangles](https://leetcode.com/problems/number-of-pairs-of-interchangeable-rectangles/)
- [Count Number of Bad Pairs](https://leetcode.com/problems/count-number-of-bad-pairs/)
- [Naming a Company](https://leetcode.com/problems/naming-a-company/)

## 47. Distance and Visit-Pattern Indexing

**Recognition:** Repeated queries ask about positions, distances, or ordered visit tuples.

**Core approach:** Pre-index occurrences or aggregate canonical visit sequences.

- [Shortest Word Distance](https://leetcode.com/problems/shortest-word-distance/)
- [Shortest Word Distance II](https://leetcode.com/problems/shortest-word-distance-ii/)
- [Analyze User Website Visit Pattern](https://leetcode.com/problems/analyze-user-website-visit-pattern/)

## 48. Union-Find Connectivity

**Recognition:** Relationships progressively merge equivalence groups.

**Core approach:** Use parent/rank with path compression, processing edges or synonym pairs before queries/generation.

- [The Earliest Moment When Everyone Becomes Friends](https://leetcode.com/problems/the-earliest-moment-when-everyone-become-friends/)
- [Synonymous Sentences](https://leetcode.com/problems/synonymous-sentences/)

## 49. Mutable 2D Range Queries

**Recognition:** Matrix values change and rectangular sums must remain efficient.

**Core approach:** Use a 2D Fenwick tree or segment tree for logarithmic updates and queries.

- [Range Sum Query 2D — Mutable](https://leetcode.com/problems/range-sum-query-2d-mutable/)

## 50. System and Data-Structure Design

**Recognition:** Maintain state across operations with explicit performance guarantees.

**Core approach:** Combine hash maps with sets, queues, heaps, timestamps, or dependency graphs as required.

- [Encode and Decode TinyURL](https://leetcode.com/problems/encode-and-decode-tinyurl/)
- [Insert Delete GetRandom O(1)](https://leetcode.com/problems/insert-delete-getrandom-o1/)
- [Design Parking System](https://leetcode.com/problems/design-parking-system/)
- [Design Underground System](https://leetcode.com/problems/design-underground-system/)
- [Design a Food Rating System](https://leetcode.com/problems/design-a-food-rating-system/)
- [Design Hit Counter](https://leetcode.com/problems/design-hit-counter/)
- [Design Phone Directory](https://leetcode.com/problems/design-phone-directory/)
- [Design Log Storage System](https://leetcode.com/problems/design-log-storage-system/)
- [Design Excel Sum Formula](https://leetcode.com/problems/design-excel-sum-formula/)

## 51. Recursive Search and Enumeration

**Recognition:** Explore combinations, orientations, substitutions, or spatial partitions.

**Core approach:** Backtrack over choices or recursively divide the search space while pruning empty regions.

- [Split Concatenated Strings](https://leetcode.com/problems/split-concatenated-strings/)
- [Number of Ships in a Rectangle](https://leetcode.com/problems/number-of-ships-in-a-rectangle/)

## Combined 175-Problem Practice Order

1. Linear scans, sets, and frequency maps
2. Pair counting and canonical keys
3. Subsequence and string comparison
4. Prefix sums and subarray counting
5. Sorting and custom comparators
6. In-place marking and array invariants
7. Sliding windows and string search
8. Grid, matrix, and sparse structures
9. Greedy array problems
10. Stream and system-design structures
11. Mutable range queries and Union-Find
12. Recursive search and advanced string problems
