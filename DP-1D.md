# Dynamic Programming Problems Segregated by Pattern

Recommended order: **Linear recurrence → Take/skip → Unbounded DP → Subsequence DP → String DP → Interval DP → State-machine DP → Bitmask DP**.

> Some problems support several approaches. Each appears under the pattern most useful for recognizing its primary DP formulation.

## 1. Linear Recurrence — Counting Ways

**Recognition:** The answer at position `i` depends on a small fixed number of earlier positions.

**Core approach:** Define `dp[i]` as the number or value of ways to reach state `i`; compress space when only recent states are needed.

- [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/)
- [N-th Tribonacci Number](https://leetcode.com/problems/n-th-tribonacci-number/)
- [Paint Fence](https://leetcode.com/problems/paint-fence/)
- [Count Ways to Build Good Strings](https://leetcode.com/problems/count-ways-to-build-good-strings/)

## 2. Linear DP — Minimum Cost

**Recognition:** Reach the end while paying the minimum cumulative cost.

**Core approach:** Let `dp[i]` represent the minimum cost to reach or finish from index `i`.

- [Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/)
- [Minimum Cost for Tickets](https://leetcode.com/problems/minimum-cost-for-tickets/)
- [Coin Path](https://leetcode.com/problems/coin-path/)

## 3. Take-or-Skip DP — Non-Adjacent Choices

**Recognition:** Choosing one element prevents choosing a neighboring or conflicting element.

**Core approach:** At each state compare taking the current value plus the next valid state against skipping it.

- [House Robber](https://leetcode.com/problems/house-robber/)
- [House Robber II](https://leetcode.com/problems/house-robber-ii/)
- [Delete and Earn](https://leetcode.com/problems/delete-and-earn/)
- [Solving Questions With Brainpower](https://leetcode.com/problems/solving-questions-with-brainpower/)

## 4. Finite-State DP

**Recognition:** Each position has a small set of modes, colors, or rule states.

**Core approach:** Define `dp[i][state]` and transition only from compatible previous states.

- [Paint House](https://leetcode.com/problems/paint-house/)
- [Student Attendance Record II](https://leetcode.com/problems/student-attendance-record-ii/)
- [Knight Dialer](https://leetcode.com/problems/knight-dialer/)

## 5. Decode and Partition DP

**Recognition:** Split a sequence into valid pieces and count or validate all possible segmentations.

**Core approach:** Let `dp[i]` describe the prefix ending at `i`; try every allowed final piece.

- [Decode Ways](https://leetcode.com/problems/decode-ways/)
- [Word Break](https://leetcode.com/problems/word-break/)
- [Check if There Is a Valid Partition for the Array](https://leetcode.com/problems/check-if-there-is-a-valid-partition-for-the-array/)
- [Concatenated Words](https://leetcode.com/problems/concatenated-words/)

## 6. Unbounded Knapsack — Minimum or Number of Combinations

**Recognition:** Items may be reused to reach a target sum.

**Core approach:** Build answers for every smaller sum; loop order determines whether order matters.

- [Coin Change](https://leetcode.com/problems/coin-change/)
- [Combination Sum IV](https://leetcode.com/problems/combination-sum-iv/)
- [Perfect Squares](https://leetcode.com/problems/perfect-squares/)
- [Integer Break](https://leetcode.com/problems/integer-break/)

## 7. 0/1 Knapsack and Subset Sum

**Recognition:** Each item can be selected at most once to reach a target.

**Core approach:** Use boolean or value DP over achievable sums, iterating sums backward for each item.

- [Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)

## 8. Maximum/Minimum Subarray State DP

**Recognition:** Find the best contiguous segment, but the transition needs more than a simple running sum.

**Core approach:** Track the relevant ending state at every position, such as both maximum and minimum products.

- [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
- [Maximum Subarray Min-Product](https://leetcode.com/problems/maximum-subarray-min-product/)

## 9. Longest Increasing Subsequence

**Recognition:** Find or count an order-preserving chain based on increasing, divisible, compatible, or predecessor relationships.

**Core approach:** Use `dp[i]` for the best chain ending at `i`, or patience sorting when only the length is required.

- [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- [Number of Longest Increasing Subsequence](https://leetcode.com/problems/number-of-longest-increasing-subsequence/)
- [Russian Doll Envelopes](https://leetcode.com/problems/russian-doll-envelopes/)
- [Best Team With No Conflicts](https://leetcode.com/problems/best-team-with-no-conflicts/)
- [Largest Divisible Subset](https://leetcode.com/problems/largest-divisible-subset/)
- [Find the Longest Valid Obstacle Course at Each Position](https://leetcode.com/problems/find-the-longest-valid-obstacle-course-at-each-position/)
- [Minimum Number of Removals to Make Mountain Array](https://leetcode.com/problems/minimum-number-of-removals-to-make-mountain-array/)

## 10. String-Chain DP

**Recognition:** Words form a chain through insertion, deletion, or another predecessor relation.

**Core approach:** Sort by length and derive each word's best state from its valid predecessors.

- [Longest String Chain](https://leetcode.com/problems/longest-string-chain/)

## 11. Palindrome DP

**Recognition:** Count, maximize, or validate palindromic substrings/subsequences.

**Core approach:** Use center expansion for contiguous palindromes; use interval DP for subsequences or deletions.

- [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- [Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/)
- [Valid Palindrome III](https://leetcode.com/problems/valid-palindrome-iii/)

## 12. Two-Sequence DP — LCS Family

**Recognition:** Match elements from two sequences while preserving relative order.

**Core approach:** Define `dp[i][j]` over prefixes; match equal elements or skip from one side.

- [Uncrossed Lines](https://leetcode.com/problems/uncrossed-lines/)

## 13. Grid and Triangle DP

**Recognition:** Choose a path through rows or a structured grid while accumulating an optimum.

**Core approach:** Derive each cell from reachable cells in the previous row; compress to one row when possible.

- [Triangle](https://leetcode.com/problems/triangle/)

## 14. Partition DP

**Recognition:** Split an array or sequence into segments, with each segment contributing a locally computed score.

**Core approach:** Let `dp[i]` be the best result for a prefix and enumerate the last segment boundary.

- [Filling Bookcase Shelves](https://leetcode.com/problems/filling-bookcase-shelves/)
- [Partition Array for Maximum Sum](https://leetcode.com/problems/partition-array-for-maximum-sum/)
- [Maximum Sum of 3 Non-Overlapping Subarrays](https://leetcode.com/problems/maximum-sum-of-3-non-overlapping-subarrays/)

## 15. Interval DP

**Recognition:** Solve every substring or range by splitting it into smaller ranges.

**Core approach:** Define `dp[left][right]`; increase interval length and try every valid split or repeated structure.

- [Encode String with Shortest Length](https://leetcode.com/problems/encode-string-with-shortest-length/)
- [Handshakes That Don't Cross](https://leetcode.com/problems/handshakes-that-dont-cross/)

## 16. Counting DP and Combinatorics

**Recognition:** Count arrangements under ordering or placement constraints.

**Core approach:** Use a counting recurrence, often strengthened by a combinatorial observation.

- [Count All Valid Pickup and Delivery Options](https://leetcode.com/problems/count-all-valid-pickup-and-delivery-options/)
- [Number of Ways to Divide a Long Corridor](https://leetcode.com/problems/number-of-ways-to-divide-a-long-corridor/)
- [Count Strictly Increasing Subarrays](https://leetcode.com/problems/count-strictly-increasing-subarrays/)

## 17. Game DP and Minimax

**Recognition:** Two optimal players alternate moves and the outcome depends on score difference.

**Core approach:** Define the maximum score advantage the current player can force from each state.

- [Stone Game III](https://leetcode.com/problems/stone-game-iii/)

## 18. Probability and Sliding-Window DP

**Recognition:** A random process transitions across a numeric range and asks for a probability.

**Core approach:** Store the probability of reaching each score and maintain the active transition sum with a sliding window.

- [New 21 Game](https://leetcode.com/problems/new-21-game/)

## 19. Sequence Generation with Multiple Pointers

**Recognition:** Generate an ordered sequence whose next value can come from several monotonic sources.

**Core approach:** Maintain one pointer per source and advance every pointer that produces the chosen minimum.

- [Ugly Number II](https://leetcode.com/problems/ugly-number-ii/)

## 20. Operation-Count DP

**Recognition:** A small set of operations builds a target, and copying changes the value of future operations.

**Core approach:** Define the best result for each operation budget or factor the target into productive copy-paste blocks.

- [4 Keys Keyboard](https://leetcode.com/problems/4-keys-keyboard/)

## 21. Screen and Cyclic String DP

**Recognition:** A repeated sentence is fitted across fixed-width rows.

**Core approach:** Precompute how far each starting word advances after one row, then reuse the transition.

- [Sentence Screen Fitting](https://leetcode.com/problems/sentence-screen-fitting/)

## 22. Bitmask DP and State Compression

**Recognition:** The state is a small subset of used items; choices depend on which items remain.

**Core approach:** Represent selected elements with a bitmask and memoize the best result for each subset.

- [Stickers to Spell Word](https://leetcode.com/problems/stickers-to-spell-word/)
- [Maximize Score After N Operations](https://leetcode.com/problems/maximize-score-after-n-operations/)

## 23. Backtracking with Memoized State

**Recognition:** Repeatedly settle, match, or eliminate values; many choice orders reach the same remaining state.

**Core approach:** Canonicalize the remaining state, try valid next moves, and memoize the minimum result.

- [Optimal Account Balancing](https://leetcode.com/problems/optimal-account-balancing/)

## 24. Weighted Interval Scheduling

**Recognition:** Jobs have start, end, and profit values; selected jobs cannot overlap.

**Core approach:** Sort jobs and combine DP with binary search for the next compatible job.

- [Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Depends on the previous few positions | Linear recurrence |
| Choose or skip conflicting values | Take-or-skip DP |
| Reuse items to reach a target | Unbounded knapsack |
| Use each item once for a target | 0/1 knapsack |
| Increasing or compatible chain | LIS |
| Match two ordered sequences | LCS |
| Split into valid prefix pieces | Partition/decode DP |
| Solve every substring or range | Interval DP |
| A few modes per position | State-machine DP |
| Two optimal players | Minimax DP |
| Random transitions across scores | Probability DP |
| Small subset of used elements | Bitmask DP |
| Profitable non-overlapping jobs | Weighted interval scheduling |

## Recommended Practice Order

1. Climbing Stairs and Tribonacci
2. Min Cost Climbing Stairs
3. House Robber I and II
4. Decode Ways and Word Break
5. Coin Change and Partition Equal Subset Sum
6. Maximum Product Subarray
7. LIS family
8. Palindrome and LCS families
9. Grid and partition DP
10. State-machine and counting DP
11. Interval, game, and probability DP
12. Bitmask DP and memoized backtracking
13. Weighted interval scheduling
