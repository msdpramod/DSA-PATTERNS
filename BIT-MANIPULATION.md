# Bit Manipulation Problems Segregated by Pattern

Recommended order: **XOR basics → Bit counting → Binary arithmetic → Prefix XOR → Range operations → Bitmask windows → Constructive bit problems**.

> Each problem is placed under the bit pattern most useful for recognizing its primary solution.

## 1. XOR Cancellation

**Recognition:** Equal values appear an even number of times, leaving one unmatched value.

**Core approach:** XOR every value; pairs cancel because `x ^ x = 0`.

- [Single Number](https://leetcode.com/problems/single-number/)
- [Missing Number](https://leetcode.com/problems/missing-number/)
- [Find the Difference](https://leetcode.com/problems/find-the-difference/)

## 2. Partition by a Distinguishing Bit

**Recognition:** Exactly two values occur once while all others occur twice.

**Core approach:** XOR everything, isolate one set bit in the combined XOR, and partition values by that bit.

- [Single Number III](https://leetcode.com/problems/single-number-iii/)

## 3. XOR Algebra and Pairing Frequency

**Recognition:** XOR is applied across every cross-array pair, and repeated participation cancels based on parity.

**Core approach:** Determine how many times each input value participates; include its XOR only when that count is odd.

- [Bitwise XOR of All Pairings](https://leetcode.com/problems/bitwise-xor-of-all-pairings/)

## 4. XOR Feasibility from Adjacent Relations

**Recognition:** An array describes XOR relationships between neighboring values in a cycle.

**Core approach:** XOR all derived relations; a valid cycle requires total cancellation.

- [Neighboring Bitwise XOR](https://leetcode.com/problems/neighboring-bitwise-xor/)

## 5. Prefix XOR and Range Queries

**Recognition:** Many queries ask for XOR over subarrays.

**Core approach:** Build prefix XOR; range XOR is `prefix[right + 1] ^ prefix[left]`.

- [XOR Queries of a Subarray](https://leetcode.com/problems/xor-queries-of-a-subarray/)

## 6. Equal-XOR Partition Counting

**Recognition:** Count triples where two adjacent ranges have equal XOR.

**Core approach:** Equal prefix XOR values imply a zero-XOR combined range; count all valid split positions between them.

- [Count Triplets That Can Form Two Arrays of Equal XOR](https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/)

## 7. XOR and Popcount Parity Counting

**Recognition:** Count tuples whose combined XOR has even/odd set-bit parity.

**Core approach:** Classify inputs by popcount parity and count parity combinations instead of enumerating all tuples.

- [Count Triplets With Even XOR Set Bits I](https://leetcode.com/problems/count-triplets-with-even-xor-set-bits-i/)

## 8. Counting Set Bits

**Recognition:** Count ones in one number or every number up to `n`.

**Core approach:** Clear the lowest set bit with `n &= n - 1`; for a range use a recurrence from `i >> 1`.

- [Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/)
- [Counting Bits](https://leetcode.com/problems/counting-bits/)

## 9. Hamming Distance and Bit Flips

**Recognition:** Count positions at which two integers differ.

**Core approach:** XOR the numbers and count set bits in the result.

- [Minimum Bit Flips to Convert Number](https://leetcode.com/problems/minimum-bit-flips-to-convert-number/)

## 10. Per-Bit Frequency

**Recognition:** The result depends on how many numbers share at least one common set bit.

**Core approach:** Count how many candidates contain each bit and take the largest count.

- [Largest Combination With Bitwise AND Greater Than Zero](https://leetcode.com/problems/largest-combination-with-bitwise-and-greater-than-zero/)

## 11. Binary Addition and Carry

**Recognition:** Add binary strings, integers without arithmetic operators, or decimal digits stored in an array.

**Core approach:** Compute result and carry per bit/digit; XOR gives sum without carry and AND-shift gives carry.

- [Add Binary](https://leetcode.com/problems/add-binary/)
- [Sum of Two Integers](https://leetcode.com/problems/sum-of-two-integers/)
- [Add to Array-Form of Integer](https://leetcode.com/problems/add-to-array-form-of-integer/)

## 12. Bit Reversal and Digit Reversal

**Recognition:** Reconstruct a value by consuming digits/bits from one side and appending them in reverse order.

**Core approach:** Shift the output and append the extracted low bit/digit while checking numeric overflow when required.

- [Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- [Reverse Integer](https://leetcode.com/problems/reverse-integer/)

## 13. Power-of-Two Test

**Recognition:** Determine whether exactly one bit is set.

**Core approach:** For positive `n`, test `(n & (n - 1)) == 0`.

- [Power of Two](https://leetcode.com/problems/power-of-two/)

## 14. Range Bitwise AND

**Recognition:** AND every number in a continuous numeric range.

**Core approach:** Right-shift both endpoints until their common binary prefix matches, then shift it back.

- [Bitwise AND of Numbers Range](https://leetcode.com/problems/bitwise-and-of-numbers-range/)

## 15. Greedy Maximum XOR per Query

**Recognition:** Choose a bounded value that maximizes XOR with the current aggregate.

**Core approach:** Within the allowed bit width, the optimal value is the bitwise complement of the aggregate XOR.

- [Maximum XOR for Each Query](https://leetcode.com/problems/maximum-xor-for-each-query/)

## 16. Shortest Window Meeting an OR Threshold

**Recognition:** Find the shortest subarray whose bitwise OR reaches at least `k`.

**Core approach:** Maintain a count for every bit in the current window so removals can reconstruct the window OR.

- [Shortest Subarray With OR at Least K II](https://leetcode.com/problems/shortest-subarray-with-or-at-least-k-ii/)

## 17. Sliding Window with Disjoint Bitmasks

**Recognition:** No bit may be set in more than one element of the window.

**Core approach:** Maintain the window OR; shrink while `windowMask & current != 0`, removing values with XOR.

- [Longest Nice Subarray](https://leetcode.com/problems/longest-nice-subarray/)

## 18. Longest Run at the Global Maximum

**Recognition:** A subarray's AND can equal the overall maximum only when every element equals that maximum.

**Core approach:** Find the global maximum and measure its longest consecutive run.

- [Longest Subarray With Maximum Bitwise AND](https://leetcode.com/problems/longest-subarray-with-maximum-bitwise-and/)

## 19. Recursive Binary-String Indexing

**Recognition:** Find one bit in a recursively defined string without constructing the full string.

**Core approach:** Compare `k` with the midpoint, then recurse into the original or reversed-inverted half.

- [Find Kth Bit in Nth Binary String](https://leetcode.com/problems/find-kth-bit-in-nth-binary-string/)

## 20. Constructive Bit Placement

**Recognition:** Construct the smallest number satisfying a required AND/XOR/popcount relationship.

**Core approach:** Place required bits first, then embed remaining bits into the lowest available zero positions.

- [Minimum Array End](https://leetcode.com/problems/minimum-array-end/)
- [Minimize XOR](https://leetcode.com/problems/minimize-xor/)

## 21. Sorting Restricted by Popcount Groups

**Recognition:** Adjacent swaps are permitted only between values with equal set-bit counts.

**Core approach:** Values cannot leave their contiguous popcount groups; verify each group can connect to the next after internal sorting.

- [Find If Array Can Be Sorted](https://leetcode.com/problems/find-if-array-can-be-sorted/)

## 22. Prefix Parity Mask

**Recognition:** Find the longest substring in which selected characters occur an even number of times.

**Core approach:** Toggle one bit per character and store the earliest index of every parity mask.

- [Find the Longest Substring Containing Vowels in Even Counts](https://leetcode.com/problems/find-the-longest-substring-containing-vowels-in-even-counts/)

## 23. Index Packing and Unpacking

**Recognition:** Rearrange values under constant-space constraints when the value range permits packing two values into one slot.

**Core approach:** Encode original and destination information together using arithmetic or bit fields, then decode.

- [Shuffle the Array](https://leetcode.com/problems/shuffle-the-array/)

## 24. IP Range Decomposition

**Recognition:** Cover a numeric IP range using the fewest aligned power-of-two blocks.

**Core approach:** Use the lowest set bit to find the largest aligned block, cap it by remaining size, and advance.

- [IP to CIDR](https://leetcode.com/problems/ip-to-cidr/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Every value paired except one | XOR all values |
| Two unpaired values | XOR + distinguishing bit |
| Many XOR range queries | Prefix XOR |
| Count differing bits | XOR + popcount |
| Add without arithmetic operators | XOR + shifted carry |
| Exactly one bit set | `n & (n - 1)` |
| AND across an integer range | Common binary prefix |
| No overlapping set bits in window | Bitmask sliding window |
| Even counts of selected characters | Prefix parity mask |
| Construct minimum with fixed bits | Fill lowest free bits |
| Cover an IP range | Aligned power-of-two blocks |

## Recommended Practice Order

1. Single Number
2. Number of 1 Bits and Counting Bits
3. Missing Number and Minimum Bit Flips
4. Add Binary and Sum of Two Integers
5. Reverse Bits and Power of Two
6. Prefix XOR queries
7. Single Number III
8. Range Bitwise AND
9. Longest Nice Subarray
10. Prefix parity masks
11. Constructive XOR and Minimum Array End
12. IP to CIDR
