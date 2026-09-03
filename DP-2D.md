# 2D and Advanced Dynamic Programming Problems by Pattern

Recommended order: **Grid DP → Knapsack → Two-sequence DP → Subsequence DP → State-machine DP → Game DP → Interval DP → Advanced multidimensional DP**.

> Some problems fit more than one family. Each appears under the pattern most useful for deriving its primary state and transition.

## 1. Grid Path Counting

**Recognition:** Count ways to move through a grid using a small set of allowed directions.

**Core approach:** Define `dp[r][c]` as the number of ways to reach or leave cell `(r,c)`; add transitions from valid neighbors.

- [Unique Paths](https://leetcode.com/problems/unique-paths/)
- [Unique Paths II](https://leetcode.com/problems/unique-paths-ii/)
- [Out of Boundary Paths](https://leetcode.com/problems/out-of-boundary-paths/)
- [Number of Ways to Stay in the Same Place After Some Steps](https://leetcode.com/problems/number-of-ways-to-stay-in-the-same-place-after-some-steps/)

## 2. Grid Minimum/Maximum Path

**Recognition:** Choose one path through a matrix while minimizing cost or maximizing points.

**Core approach:** Store the best result ending at each cell; compress rows when only the previous row is required.

- [Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- [Minimum Falling Path Sum](https://leetcode.com/problems/minimum-falling-path-sum/)
- [Minimum Falling Path Sum II](https://leetcode.com/problems/minimum-falling-path-sum-ii/)
- [Maximum Number of Points With Cost](https://leetcode.com/problems/maximum-number-of-points-with-cost/)

## 3. Matrix Shape DP

**Recognition:** Find or count all-ones squares ending at each cell.

**Core approach:** For a `1` cell, use one plus the minimum of its top, left, and top-left states.

- [Maximal Square](https://leetcode.com/problems/maximal-square/)
- [Count Square Submatrices With All Ones](https://leetcode.com/problems/count-square-submatrices-with-all-ones/)

## 4. DAG and Memoized Matrix DP

**Recognition:** Moves are permitted only when values satisfy a strict order, making the implicit graph acyclic.

**Core approach:** Run DFS with memoization from each cell, or process cells in topological value order.

- [Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)

## 5. 0/1 Knapsack and Subset Sum

**Recognition:** Each item is used at most once to reach a sum, difference, or selection target.

**Core approach:** Use DP over achievable totals; iterate capacities backward to prevent reusing an item.

- [Last Stone Weight II](https://leetcode.com/problems/last-stone-weight-ii/)
- [Target Sum](https://leetcode.com/problems/target-sum/)
- [Split Array With Same Average](https://leetcode.com/problems/split-array-with-same-average/)

## 6. Multidimensional Knapsack

**Recognition:** Each choice consumes two or more limited resources.

**Core approach:** Let each DP dimension represent one capacity or requirement, and update capacities backward for 0/1 choices.

- [Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/)
- [Profitable Schemes](https://leetcode.com/problems/profitable-schemes/)
- [Painting the Walls](https://leetcode.com/problems/painting-the-walls/)

## 7. Unbounded and Group Knapsack

**Recognition:** Values may be reused, or exactly one prefix/quantity is selected from each group.

**Core approach:** Build target totals progressively; for grouped choices, enumerate how many items to take from the current group.

- [Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- [Number of Dice Rolls With Target Sum](https://leetcode.com/problems/number-of-dice-rolls-with-target-sum/)
- [Maximum Value of K Coins From Piles](https://leetcode.com/problems/maximum-value-of-k-coins-from-piles/)

## 8. Longest Common Subsequence Family

**Recognition:** Match two ordered sequences without requiring contiguous positions.

**Core approach:** Define `dp[i][j]` over prefixes; match equal elements or skip one side.

- [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
- [Shortest Common Supersequence](https://leetcode.com/problems/shortest-common-supersequence/)
- [Interleaving String](https://leetcode.com/problems/interleaving-string/)

## 9. Counting Subsequences Across Two Sequences

**Recognition:** Count how many ways one string or sequence can form another while preserving order.

**Core approach:** Use prefix DP; when symbols match, combine using and skipping the current source symbol.

- [Distinct Subsequences](https://leetcode.com/problems/distinct-subsequences/)
- [Number of Ways to Form a Target String Given a Dictionary](https://leetcode.com/problems/number-of-ways-to-form-a-target-string-given-a-dictionary/)

## 10. Edit and Pattern-Matching DP

**Recognition:** Transform one string into another or match it against operators such as `.` and `*`.

**Core approach:** Define states over prefixes and model each allowed edit or pattern operator explicitly.

- [Edit Distance](https://leetcode.com/problems/edit-distance/)
- [Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/)

## 11. Palindromic Subsequence DP

**Recognition:** Find the best palindrome that preserves order but may skip characters.

**Core approach:** Use interval DP: match equal endpoints or discard one endpoint.

- [Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/)

## 12. Subsequence-State DP

**Recognition:** The best subsequence depends on a small property of its last element, difference, parity, or position.

**Core approach:** Store the best or count of subsequences ending in each relevant state.

- [Length of Longest Fibonacci Subsequence](https://leetcode.com/problems/length-of-longest-fibonacci-subsequence/)
- [Maximum Alternating Subsequence Sum](https://leetcode.com/problems/maximum-alternating-subsequence-sum/)
- [Longest Ideal Subsequence](https://leetcode.com/problems/longest-ideal-subsequence/)
- [Count Number of Teams](https://leetcode.com/problems/count-number-of-teams/)
- [Arithmetic Slices II — Subsequence](https://leetcode.com/problems/arithmetic-slices-ii-subsequence/)

## 13. Finite-State and Transition DP

**Recognition:** Each step moves among a small fixed set of modes.

**Core approach:** Define `dp[i][state]` and transition from every compatible previous state.

- [Best Time to Buy and Sell Stock With Cooldown](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- [Count Vowels Permutation](https://leetcode.com/problems/count-vowels-permutation/)
- [Flip String to Monotone Increasing](https://leetcode.com/problems/flip-string-to-monotone-increasing/)
- [Paint House II](https://leetcode.com/problems/paint-house-ii/)

## 14. Game DP and Minimax

**Recognition:** Two optimal players alternately take actions from a shared state.

**Core approach:** Store the maximum score advantage or best achievable score for the current player.

- [Stone Game](https://leetcode.com/problems/stone-game/)
- [Stone Game II](https://leetcode.com/problems/stone-game-ii/)

## 15. Interval DP — Choose the Last Action

**Recognition:** Performing an action splits a range into independent left and right ranges.

**Core approach:** Define `dp[left][right]` and try every possible final balloon, cut, or partition point.

- [Burst Balloons](https://leetcode.com/problems/burst-balloons/)
- [Minimum Cost to Cut a Stick](https://leetcode.com/problems/minimum-cost-to-cut-a-stick/)

## 16. Partition DP — Jobs and Segments

**Recognition:** Split an ordered list into a fixed number of contiguous groups while optimizing group cost.

**Core approach:** Define DP by prefix and group count; enumerate the start of the final group.

- [Minimum Difficulty of a Job Schedule](https://leetcode.com/problems/minimum-difficulty-of-a-job-schedule/)

## 17. String Compression DP

**Recognition:** Delete a limited number of characters to minimize run-length encoded size.

**Core approach:** Memoize by position, deletions remaining, previous character, and run length—or enumerate the next retained group.

- [String Compression II](https://leetcode.com/problems/string-compression-ii/)

## 18. Combinatorial Counting DP

**Recognition:** Count permutations or arrangements subject to visibility, repetition, or inversion constraints.

**Core approach:** Add one element and count how its placement changes the tracked statistic.

- [Number of Ways to Rearrange Sticks With K Sticks Visible](https://leetcode.com/problems/number-of-ways-to-rearrange-sticks-with-k-sticks-visible/)
- [Number of Music Playlists](https://leetcode.com/problems/number-of-music-playlists/)
- [K Inverse Pairs Array](https://leetcode.com/problems/k-inverse-pairs-array/)

## 19. Operation DP and Factorization

**Recognition:** A small set of copy/paste-style operations must construct a target with minimum cost.

**Core approach:** Use DP over constructed length or derive the optimum through prime factorization.

- [2 Keys Keyboard](https://leetcode.com/problems/2-keys-keyboard/)

## 20. Circular Position DP

**Recognition:** Select characters or targets by rotating around a ring.

**Core approach:** Memoize by target index and current ring position; try every matching next position.

- [Freedom Trail](https://leetcode.com/problems/freedom-trail/)

## 21. Two-Agent Grid DP

**Recognition:** Two travelers move through a grid simultaneously, and shared cells must not be counted twice.

**Core approach:** Advance both travelers by the same step count and memoize their combined positions.

- [Cherry Pickup](https://leetcode.com/problems/cherry-pickup/)
- [Cherry Pickup II](https://leetcode.com/problems/cherry-pickup-ii/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Count paths through cells | Grid counting DP |
| Cheapest/best matrix path | Grid optimization DP |
| Largest all-ones square | Local matrix-shape DP |
| Increasing moves in a matrix | DFS + memoization |
| Use each item once for a total | 0/1 knapsack |
| Multiple resource limits | Multidimensional knapsack |
| Reuse values or select from piles | Unbounded/group knapsack |
| Match two ordered sequences | LCS-style DP |
| Count ways to form a target string | Two-sequence counting DP |
| Transform or regex-match strings | Edit/pattern DP |
| Subsequence depends on last state | Subsequence-state DP |
| Small modes at every step | State-machine DP |
| Two optimal players | Minimax DP |
| Action splits a range | Interval DP |
| Split list into contiguous groups | Partition DP |
| Two simultaneous grid travelers | Multi-agent grid DP |

## Recommended Practice Order

1. Unique Paths and Minimum Path Sum
2. Falling-path and square-matrix DP
3. Coin Change II and subset-sum variants
4. LCS and Interleaving String
5. Distinct Subsequences and Edit Distance
6. Subsequence-state DP
7. Stock and finite-state DP
8. Stone games
9. Burst Balloons and Cut a Stick
10. Combinatorial and partition DP
11. Freedom Trail and String Compression II
12. Cherry Pickup I and II
