# Stack and Monotonic Stack Problems Segregated by Pattern

Recommended order: **Stack simulation → Parentheses → String cancellation → Expression parsing → Monotonic stack → Contribution counting → Monotonic deque**.

> Some problems allow several techniques. Each appears under the stack pattern most useful for recognizing its primary solution.

## 1. Basic Stack Simulation

**Recognition:** Operations undo, replace, or depend on the most recent unresolved item.

**Core approach:** Translate every operation into push, pop, or inspect-top behavior.

- [Crawler Log Folder](https://leetcode.com/problems/crawler-log-folder/)
- [Baseball Game](https://leetcode.com/problems/baseball-game/)
- [Validate Stack Sequences](https://leetcode.com/problems/validate-stack-sequences/)

## 2. Parentheses Validation and Balancing

**Recognition:** Brackets must close in reverse opening order, or missing parentheses must be counted.

**Core approach:** Push opening symbols and match closings; when only one bracket type exists, a balance counter may replace the stack.

- [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- [Minimum Add to Make Parentheses Valid](https://leetcode.com/problems/minimum-add-to-make-parentheses-valid/)

## 3. Implement One Linear Structure Using Another

**Recognition:** Implement stack behavior with queues or queue behavior with stacks.

**Core approach:** Make either insertion or removal expensive while preserving the target structure's order.

- [Implement Stack Using Queues](https://leetcode.com/problems/implement-stack-using-queues/)
- [Implement Queue Using Stacks](https://leetcode.com/problems/implement-queue-using-stacks/)

## 4. Stack with Constant-Time Aggregate

**Recognition:** Standard stack operations plus minimum or maximum queries must all be efficient.

**Core approach:** Store an auxiliary aggregate with each entry, or maintain a synchronized second stack.

- [Min Stack](https://leetcode.com/problems/min-stack/)
- [Max Stack](https://leetcode.com/problems/max-stack/)

## 5. Frequency-Ordered Stack

**Recognition:** Pop the most frequent item, breaking ties by recency.

**Core approach:** Map values to frequencies and frequencies to stacks; track the current maximum frequency.

- [Maximum Frequency Stack](https://leetcode.com/problems/maximum-frequency-stack/)

## 6. Adjacent String Cancellation

**Recognition:** Adjacent characters or substrings repeatedly eliminate one another.

**Core approach:** Treat the output buffer as a stack; after every append, test whether the top now forms a removable pattern.

- [Make the String Great](https://leetcode.com/problems/make-the-string-great/)
- [Removing Stars From a String](https://leetcode.com/problems/removing-stars-from-a-string/)
- [Remove All Adjacent Duplicates in String II](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string-ii/)
- [Minimum String Length After Removing Substrings](https://leetcode.com/problems/minimum-string-length-after-removing-substrings/)
- [Clear Digits](https://leetcode.com/problems/clear-digits/)

## 7. Reverse Polish Notation

**Recognition:** Operators follow their operands.

**Core approach:** Push numbers; on an operator pop the right operand and then the left operand, evaluate, and push the result.

- [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/)

## 8. Infix Expression Evaluation

**Recognition:** Evaluate infix arithmetic with precedence and possibly nested parentheses.

**Core approach:** Maintain operand/operator stacks or use recursive descent, applying higher-precedence operations first.

- [Basic Calculator II](https://leetcode.com/problems/basic-calculator-ii/)
- [Basic Calculator III](https://leetcode.com/problems/basic-calculator-iii/)

## 9. Nested Expression and Grammar Parsing

**Recognition:** Nested delimiters define repeated strings, ternary branches, Boolean groups, or chemical formulas.

**Core approach:** Push outer context at each opening delimiter and collapse the completed inner expression at its closing delimiter.

- [Decode String](https://leetcode.com/problems/decode-string/)
- [Ternary Expression Parser](https://leetcode.com/problems/ternary-expression-parser/)
- [Parsing a Boolean Expression](https://leetcode.com/problems/parsing-a-boolean-expression/)
- [Number of Atoms](https://leetcode.com/problems/number-of-atoms/)

## 10. Parenthesized String Transformation

**Recognition:** Each matched pair triggers a transformation of its enclosed substring.

**Core approach:** Use a stack of partial strings or precompute matching parentheses and traverse with direction changes.

- [Reverse Substrings Between Each Pair of Parentheses](https://leetcode.com/problems/reverse-substrings-between-each-pair-of-parentheses/)

## 11. Path Canonicalization

**Recognition:** Resolve parent-directory and current-directory tokens.

**Core approach:** Split by separators and use a stack of valid directory names.

- [Simplify Path](https://leetcode.com/problems/simplify-path/)

## 12. Nested Iterator

**Recognition:** Expose a recursively nested structure through a flat iterator interface.

**Core approach:** Store pending nested elements on a stack and lazily expand lists until the top is an integer.

- [Flatten Nested List Iterator](https://leetcode.com/problems/flatten-nested-list-iterator/)

## 13. Collision Simulation

**Recognition:** Ordered objects move toward one another; only unresolved objects can collide with the next one.

**Core approach:** Keep surviving objects on a stack and repeatedly resolve conflicts against the top.

- [Asteroid Collision](https://leetcode.com/problems/asteroid-collision/)
- [Robot Collisions](https://leetcode.com/problems/robot-collisions/)

## 14. Next Smaller/Greater Element

**Recognition:** For each item, find the first later item that is smaller, greater, warmer, or otherwise resolves it.

**Core approach:** Maintain indices whose answers are unresolved in monotonic order; the current item pops and resolves them.

- [Final Prices With a Special Discount in a Shop](https://leetcode.com/problems/final-prices-with-a-special-discount-in-a-shop/)
- [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
- [Online Stock Span](https://leetcode.com/problems/online-stock-span/)
- [Number of Visible People in a Queue](https://leetcode.com/problems/number-of-visible-people-in-a-queue/)

## 15. Monotonic Stack over Sorted Positions

**Recognition:** Entities start at sorted positions and merge when a later one catches an earlier group.

**Core approach:** Sort by position, convert to arrival times, and maintain fleets as a monotonic sequence.

- [Car Fleet](https://leetcode.com/problems/car-fleet/)

## 16. Greedy Monotonic Stack

**Recognition:** Remove or choose elements to construct the lexicographically smallest/largest valid result.

**Core approach:** While the top is worse than the current candidate and removals remain, pop it.

- [Remove K Digits](https://leetcode.com/problems/remove-k-digits/)
- [Find Permutation](https://leetcode.com/problems/find-permutation/)

## 17. Pattern Detection with a Monotonic Stack

**Recognition:** Detect three indices satisfying a relative-order pattern rather than simple adjacent comparison.

**Core approach:** Scan from the right, maintain possible high values on a decreasing stack, and track the best middle value.

- [132 Pattern](https://leetcode.com/problems/132-pattern/)

## 18. Monotonic Boundary and Contribution Counting

**Recognition:** Each element contributes across the range where it remains the minimum, maximum, or limiting height.

**Core approach:** Find previous/next smaller boundaries and compute the span controlled by each element.

- [Sum of Subarray Minimums](https://leetcode.com/problems/sum-of-subarray-minimums/)
- [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)

## 19. Maximum-Width Pair with Monotonic Candidates

**Recognition:** Maximize `j - i` subject to an inequality between values at the two indices.

**Core approach:** Store decreasing candidate left indices, then scan right indices backward and pop every satisfied candidate.

- [Maximum Width Ramp](https://leetcode.com/problems/maximum-width-ramp/)

## 20. Monotonic Deque over Prefix Sums

**Recognition:** Find the shortest subarray meeting a sum threshold when negative numbers prevent a normal sliding window.

**Core approach:** Maintain prefix-sum indices in increasing order; pop from the front when the threshold is met and from the back when dominated.

- [Shortest Subarray With Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Undo or recent unresolved operation | Basic stack |
| Match nested brackets | Parentheses stack |
| Adjacent characters disappear | Output-buffer stack |
| Postfix expression | Operand stack |
| Infix operators and precedence | Operator/operand stacks |
| Nested grammar or delimiters | Context stack |
| Moving objects collide | Survivor stack |
| First later greater/smaller item | Monotonic stack |
| Remove digits/items greedily | Monotonic greedy stack |
| Contribution as min/max over ranges | Previous/next boundary stack |
| Shortest threshold sum with negatives | Prefix sums + monotonic deque |

## Recommended Practice Order

1. Valid Parentheses
2. Min Stack
3. Evaluate Reverse Polish Notation
4. Adjacent string cancellation
5. Decode String and Simplify Path
6. Asteroid Collision
7. Daily Temperatures and Stock Span
8. Remove K Digits
9. Car Fleet and 132 Pattern
10. Largest Rectangle in Histogram
11. Sum of Subarray Minimums
12. Shortest Subarray With Sum at Least K
