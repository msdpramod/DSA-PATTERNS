# Backtracking Problems Segregated by Pattern

Recommended order: **Subsets → Combinations → Permutations → String construction → Partitioning → Grid search → Constraint placement → Advanced state search**.

> Some problems support multiple techniques. Each appears under the backtracking pattern most useful for recognizing its search tree.

## 1. Include-or-Exclude Subsets

**Recognition:** Generate or evaluate every subset of a collection.

**Core approach:** At index `i`, either include the element or skip it; process the result at the leaf or during traversal.

- [Subsets](https://leetcode.com/problems/subsets/)
- [Sum of All Subset XOR Totals](https://leetcode.com/problems/sum-of-all-subset-xor-totals/)
- [Count Number of Maximum Bitwise-OR Subsets](https://leetcode.com/problems/count-number-of-maximum-bitwise-or-subsets/)

## 2. Subsets with Duplicate Handling

**Recognition:** Input contains duplicates, but the result must contain unique subsets.

**Core approach:** Sort first, then skip equal candidates at the same recursion depth.

- [Subsets II](https://leetcode.com/problems/subsets-ii/)
- [The Number of Beautiful Subsets](https://leetcode.com/problems/the-number-of-beautiful-subsets/)

## 3. Fixed-Size Combinations

**Recognition:** Choose exactly `k` values without regard to order.

**Core approach:** Pass a forward-only start index and prune when too few candidates remain.

- [Combinations](https://leetcode.com/problems/combinations/)

## 4. Target-Sum Combinations

**Recognition:** Select candidates whose sum equals a target.

**Core approach:** Track the remaining target; decide whether candidates can be reused and skip duplicates at the same depth when necessary.

- [Combination Sum](https://leetcode.com/problems/combination-sum/)
- [Combination Sum II](https://leetcode.com/problems/combination-sum-ii/)

## 5. Permutations and Used-State Tracking

**Recognition:** Generate every ordering, so position matters.

**Core approach:** Build one position at a time using a `used` array or in-place swapping.

- [Permutations](https://leetcode.com/problems/permutations/)
- [Letter Tile Possibilities](https://leetcode.com/problems/letter-tile-possibilities/)

## 6. Unique Permutations with Duplicates

**Recognition:** Generate distinct orderings from repeated values.

**Core approach:** Sort and use a `used` array; skip an equal value when its identical predecessor has not been used in the current branch.

- [Permutations II](https://leetcode.com/problems/permutations-ii/)

## 7. Constrained Sequence Construction

**Recognition:** Construct a sequence that obeys adjacency, spacing, comparison, or uniqueness rules.

**Core approach:** Fill positions left to right, try candidates in the output-priority order, and prune invalid partial sequences immediately.

- [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/)
- [The K-th Lexicographical String of All Happy Strings of Length n](https://leetcode.com/problems/the-k-th-lexicographical-string-of-all-happy-strings-of-length-n/)
- [Construct Smallest Number From DI String](https://leetcode.com/problems/construct-smallest-number-from-di-string/)
- [Find Unique Binary String](https://leetcode.com/problems/find-unique-binary-string/)
- [Construct the Lexicographically Largest Valid Sequence](https://leetcode.com/problems/construct-the-lexicographically-largest-valid-sequence/)
- [Strobogrammatic Number II](https://leetcode.com/problems/strobogrammatic-number-ii/)
- [Android Unlock Patterns](https://leetcode.com/problems/android-unlock-patterns/)

## 8. Choice Expansion from Character Groups

**Recognition:** Each input position offers a small independent set of character choices.

**Core approach:** Pick one option for the current position and recurse to the next.

- [Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
- [Brace Expansion](https://leetcode.com/problems/brace-expansion/)

## 9. String Partitioning

**Recognition:** Split a string into pieces satisfying a validation rule.

**Core approach:** Try every next endpoint, validate the chosen piece, then recurse on the remaining suffix.

- [Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning/)
- [Restore IP Addresses](https://leetcode.com/problems/restore-ip-addresses/)
- [Splitting a String Into Descending Consecutive Values](https://leetcode.com/problems/splitting-a-string-into-descending-consecutive-values/)
- [Split a String Into the Max Number of Unique Substrings](https://leetcode.com/problems/split-a-string-into-the-max-number-of-unique-substrings/)
- [Word Break II](https://leetcode.com/problems/word-break-ii/)

## 10. Grid Backtracking

**Recognition:** Search a path through neighboring cells while preventing reuse within the same path.

**Core approach:** Mark the current cell, explore neighbors, and restore it when returning.

- [Word Search](https://leetcode.com/problems/word-search/)

## 11. Bucket and Equal-Partition Assignment

**Recognition:** Assign all items to a fixed number of groups with equal capacity or balanced totals.

**Core approach:** Sort descending, place each item into a valid bucket, and skip equivalent bucket states.

- [Matchsticks to Square](https://leetcode.com/problems/matchsticks-to-square/)
- [Partition to K Equal Sum Subsets](https://leetcode.com/problems/partition-to-k-equal-sum-subsets/)

## 12. Unique-Character and Resource-Constrained Selection

**Recognition:** Select a subset of words/strings while respecting character availability or uniqueness.

**Core approach:** Maintain a bitmask or frequency array representing resources already used.

- [Maximum Length of a Concatenated String With Unique Characters](https://leetcode.com/problems/maximum-length-of-a-concatenated-string-with-unique-characters/)
- [Maximum Score Words Formed by Letters](https://leetcode.com/problems/maximum-score-words-formed-by-letters/)

## 13. Divide-and-Conquer Expression Enumeration

**Recognition:** Parenthesizing an expression differently produces multiple valid results.

**Core approach:** Choose each operator as the final split and combine every result from its left and right subexpressions.

- [Different Ways to Add Parentheses](https://leetcode.com/problems/different-ways-to-add-parentheses/)

## 14. Factor Decomposition

**Recognition:** Generate multiplicative combinations whose product equals the target.

**Core approach:** Try divisors from a nondecreasing start value to avoid reordered duplicates.

- [Factor Combinations](https://leetcode.com/problems/factor-combinations/)

## 15. Bijection and Mapping Backtracking

**Recognition:** Pattern symbols must map consistently and uniquely to substrings.

**Core approach:** Maintain both the forward mapping and a set of already-used target substrings.

- [Word Pattern II](https://leetcode.com/problems/word-pattern-ii/)

## 16. Constraint Placement — Rows, Columns, and Diagonals

**Recognition:** Place pieces so that no two conflict across several dimensions.

**Core approach:** Place one row at a time and maintain occupied columns and diagonals with sets or bitmasks.

- [N-Queens](https://leetcode.com/problems/n-queens/)
- [N-Queens II](https://leetcode.com/problems/n-queens-ii/)

## 17. Unknown-Environment Exploration

**Recognition:** The grid is hidden behind movement APIs and must be explored while physically restoring position.

**Core approach:** DFS through available directions; after exploring a branch, issue the reverse move to return to the prior state.

- [Robot Room Cleaner](https://leetcode.com/problems/robot-room-cleaner/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Every subset | Include/exclude |
| Choose exactly K items | Forward-index combinations |
| Sum to target | Remaining-target recursion |
| Every ordering | Permutations + used state |
| Duplicate input, unique output | Sort + same-level skip |
| Balanced groups or buckets | Bucket assignment |
| Split a string into valid pieces | Endpoint partitioning |
| Path through neighboring cells | Grid DFS + restore |
| Character uniqueness/resources | Bitmask or frequency state |
| Different expression groupings | Divide and conquer |
| Symbol-to-substring mapping | Bidirectional uniqueness |
| Non-conflicting board placement | Columns/diagonals sets |
| Hidden movement interface | DFS + physical backtracking |

## Recommended Practice Order

1. Subsets
2. Combinations
3. Permutations
4. Combination Sum I and II
5. Subsets II and Permutations II
6. Generate Parentheses
7. Phone Letter Combinations
8. Palindrome Partitioning and Restore IP Addresses
9. Word Search
10. Matchsticks to Square and K Equal Sum Subsets
11. Unique-character selection problems
12. N-Queens
13. Expression, mapping, and environment-search problems
