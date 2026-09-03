# Sliding Window Problems Segregated by Pattern

Recommended order: **Fixed window → Variable window → Frequency constraints → Exact-count windows → Circular windows → Monotonic deque → Multi-list windows**.

> Some problems support multiple approaches. Each appears under the sliding-window pattern most useful for recognizing its primary solution.

## 1. Fixed-Size Window — Running Count or Sum

**Recognition:** Inspect every contiguous block of exactly `k` elements.

**Core approach:** Build the first window, then add the entering element and remove the leaving element in `O(1)`.

- [Minimum Recolors to Get K Consecutive Black Blocks](https://leetcode.com/problems/minimum-recolors-to-get-k-consecutive-black-blocks/)
- [Number of Sub-arrays of Size K and Average Greater Than or Equal to Threshold](https://leetcode.com/problems/number-of-sub-arrays-of-size-k-and-average-greater-than-or-equal-to-threshold/)
- [Grumpy Bookstore Owner](https://leetcode.com/problems/grumpy-bookstore-owner/)
- [Maximum Number of Vowels in a Substring of Given Length](https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/)
- [Find the Power of K-Size Subarrays I](https://leetcode.com/problems/find-the-power-of-k-size-subarrays-i/)

## 2. Fixed Window with Frequency Map

**Recognition:** Every length-`k` window must satisfy a uniqueness or frequency condition.

**Core approach:** Maintain counts for the current window and update a duplicate/distinct counter as endpoints move.

- [Contains Duplicate II](https://leetcode.com/problems/contains-duplicate-ii/)
- [Find K-Length Substrings With No Repeated Characters](https://leetcode.com/problems/find-k-length-substrings-with-no-repeated-characters/)
- [Maximum Sum of Distinct Subarrays With Length K](https://leetcode.com/problems/maximum-sum-of-distinct-subarrays-with-length-k/)

## 3. Minimum/Maximum over Sorted Windows

**Recognition:** After sorting, the desired subset becomes a contiguous block.

**Core approach:** Sort first and inspect every relevant window of values.

- [Minimum Difference Between Highest and Lowest of K Scores](https://leetcode.com/problems/minimum-difference-between-highest-and-lowest-of-k-scores/)
- [Find K Closest Elements](https://leetcode.com/problems/find-k-closest-elements/)
- [Maximum Beauty of an Array After Applying Operation](https://leetcode.com/problems/maximum-beauty-of-an-array-after-applying-operation/)
- [Minimum Number of Operations to Make Array Continuous](https://leetcode.com/problems/minimum-number-of-operations-to-make-array-continuous/)

## 4. One-Pass Running Minimum

**Recognition:** Maximize a later-minus-earlier value while preserving order.

**Core approach:** Track the minimum value seen before the current position and update the best difference.

- [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

## 5. Longest Window with Bounded Distinct Values

**Recognition:** Find the longest substring/subarray containing at most `k` distinct values.

**Core approach:** Expand right, count frequencies, and shrink left while the distinct count exceeds the limit.

- [Longest Substring With at Most Two Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-two-distinct-characters/)
- [Longest Substring With at Most K Distinct Characters](https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/)
- [Fruit Into Baskets](https://leetcode.com/problems/fruit-into-baskets/)

## 6. Longest Window Without Repetition or Excess Frequency

**Recognition:** Every value may occur at most once or at most `k` times.

**Core approach:** Track last positions or frequencies and shrink until the duplicated/over-limit value becomes valid.

- [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- [Length of Longest Subarray With at Most K Frequency](https://leetcode.com/problems/length-of-longest-subarray-with-at-most-k-frequency/)

## 7. Replacement and Flip Budget

**Recognition:** A limited number of changes may make a window uniform or valid.

**Core approach:** Maintain the number of changes required; shrink only when it exceeds the budget.

- [Max Consecutive Ones II](https://leetcode.com/problems/max-consecutive-ones-ii/)
- [Max Consecutive Ones III](https://leetcode.com/problems/max-consecutive-ones-iii/)
- [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
- [Get Equal Substrings Within Budget](https://leetcode.com/problems/get-equal-substrings-within-budget/)

## 8. Fixed-Frequency Anagram Window

**Recognition:** A substring must have exactly the same character multiset as a pattern.

**Core approach:** Use a fixed-length frequency window and track whether all count differences are zero.

- [Permutation in String](https://leetcode.com/problems/permutation-in-string/)

## 9. Minimum Valid Window

**Recognition:** Find the shortest substring that satisfies all required character counts.

**Core approach:** Expand until valid, then shrink greedily while preserving validity.

- [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)

## 10. Positive-Number Sum or Product Window

**Recognition:** All values are positive, making sum/product monotonic as the window expands or shrinks.

**Core approach:** Expand right and shrink left until the threshold condition becomes valid; count or minimize from there.

- [Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
- [Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)

## 11. Exact Count via At-Most Windows

**Recognition:** Count subarrays containing exactly `k` odd values, distinct values, consonants, or target sum in binary data.

**Core approach:** Compute `atMost(k) - atMost(k - 1)`, or use equivalent prefix-frequency counting when appropriate.

- [Binary Subarrays With Sum](https://leetcode.com/problems/binary-subarrays-with-sum/)
- [Count Number of Nice Subarrays](https://leetcode.com/problems/count-number-of-nice-subarrays/)
- [Subarrays With K Different Integers](https://leetcode.com/problems/subarrays-with-k-different-integers/)
- [Count of Substrings Containing Every Vowel and K Consonants II](https://leetcode.com/problems/count-of-substrings-containing-every-vowel-and-k-consonants-ii/)

## 12. Count Windows after Reaching a Required Set

**Recognition:** Count substrings containing every required symbol or at least `k` copies of a special value.

**Core approach:** Once a window is valid, count all extensions or all valid starting positions in bulk.

- [Number of Substrings Containing All Three Characters](https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/)
- [Count Subarrays Where Max Element Appears at Least K Times](https://leetcode.com/problems/count-subarrays-where-max-element-appears-at-least-k-times/)

## 13. Complementary Window

**Recognition:** Operations remove elements from both ends, so the unremoved middle is contiguous.

**Core approach:** Convert the goal into finding the longest middle window with a required sum or allowable character counts.

- [Minimum Operations to Reduce X to Zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/)
- [Take K of Each Character From Left and Right](https://leetcode.com/problems/take-k-of-each-character-from-left-and-right/)

## 14. Frequency Equalization after Sorting

**Recognition:** Increase values within a budget to make as many of them equal as possible.

**Core approach:** Sort, maintain the window sum, and compare the cost of raising every value to the current rightmost value.

- [Frequency of the Most Frequent Element](https://leetcode.com/problems/frequency-of-the-most-frequent-element/)

## 15. Circular Sliding Window

**Recognition:** The array/string wraps around, so a valid window may cross the physical boundary.

**Core approach:** Traverse indices modulo `n` or logically duplicate the sequence while limiting window length.

- [Alternating Groups II](https://leetcode.com/problems/alternating-groups-ii/)
- [Minimum Number of Flips to Make the Binary String Alternating](https://leetcode.com/problems/minimum-number-of-flips-to-make-the-binary-string-alternating/)
- [Defuse the Bomb](https://leetcode.com/problems/defuse-the-bomb/)

## 16. Monotonic Deque — Window Maximum

**Recognition:** Query the maximum or minimum of every fixed-size window.

**Core approach:** Store candidate indices in decreasing/increasing value order and discard expired or dominated indices.

- [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)

## 17. Two Monotonic Deques — Bounded Range

**Recognition:** The window is valid while `max - min` stays within a limit.

**Core approach:** Maintain a decreasing max deque and increasing min deque, shrinking when their difference exceeds the bound.

- [Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit](https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/)

## 18. Smallest Range Across K Lists

**Recognition:** Choose at least one element from every sorted list while minimizing the overall range.

**Core approach:** Maintain one pointer per list with a min-heap and track the maximum currently selected value.

- [Smallest Range Covering Elements From K Lists](https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Every block has exactly K elements | Fixed window |
| Longest window with a frequency limit | Variable window |
| At most K distinct values | Frequency-map window |
| Limited replacements or flips | Budget window |
| Same multiset as a pattern | Fixed anagram window |
| Shortest window covering requirements | Minimum valid window |
| Positive sum/product threshold | Two-pointer window |
| Exactly K occurrences/distinct values | At-most difference |
| Take values from both ends | Complementary middle window |
| Sequence wraps around | Circular window |
| Maximum for each window | Monotonic deque |
| Bound on max minus min | Two deques |
| One element from every sorted list | Heap-based K-list window |

## Recommended Practice Order

1. Fixed-size running-sum windows
2. Longest Substring Without Repeating Characters
3. Fruit Into Baskets
4. Character Replacement and Max Consecutive Ones
5. Permutation in String
6. Minimum Size Subarray Sum
7. Minimum Window Substring
8. Exact-K counting through at-most windows
9. Complementary-window problems
10. Circular windows
11. Sliding Window Maximum
12. Longest Continuous Subarray
13. Smallest Range Covering K Lists
