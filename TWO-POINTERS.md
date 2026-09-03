# Two-Pointer Problems Segregated by Pattern

Recommended order: **Opposite ends → Read/write pointers → Parallel traversal → Sorted pair search → K-sum → Greedy pairing → Boundary optimization**.

> Each problem is placed under the two-pointer pattern most useful for recognizing its primary solution.

## 1. Opposite-End String Processing

**Recognition:** Compare, swap, or remove characters from both ends.

**Core approach:** Move left and right pointers inward while skipping, comparing, or swapping characters.

- [Reverse String](https://leetcode.com/problems/reverse-string/)
- [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- [Find First Palindromic String in the Array](https://leetcode.com/problems/find-first-palindromic-string-in-the-array/)
- [Reverse Words in a String III](https://leetcode.com/problems/reverse-words-in-a-string-iii/)
- [Strobogrammatic Number](https://leetcode.com/problems/strobogrammatic-number/)

## 2. Palindrome with One Allowed Deletion

**Recognition:** A string may become a palindrome after removing at most one character.

**Core approach:** On the first mismatch, test the ranges obtained by skipping either endpoint.

- [Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/)

## 3. Inward Removal of Matching Ends

**Recognition:** Equal character groups can be deleted simultaneously from both ends.

**Core approach:** When endpoints match, consume the complete matching run on both sides.

- [Minimum Length of String After Deleting Similar Ends](https://leetcode.com/problems/minimum-length-of-string-after-deleting-similar-ends/)

## 4. Parallel String Traversal

**Recognition:** Two logical strings or token sequences must be compared without fully constructing them.

**Core approach:** Maintain one pointer per sequence and advance through segments, words, or ignored characters.

- [Valid Word Abbreviation](https://leetcode.com/problems/valid-word-abbreviation/)
- [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
- [Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)
- [Check If Two String Arrays Are Equivalent](https://leetcode.com/problems/check-if-two-string-arrays-are-equivalent/)
- [Adding Spaces to a String](https://leetcode.com/problems/adding-spaces-to-a-string/)
- [Sentence Similarity III](https://leetcode.com/problems/sentence-similarity-iii/)

## 5. Merge Two Sorted Sequences

**Recognition:** Two ordered inputs must be combined or intersected.

**Core approach:** Compare current values and advance the pointer whose value or interval ends first.

- [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
- [Merge Two 2D Arrays by Summing Values](https://leetcode.com/problems/merge-two-2d-arrays-by-summing-values/)
- [Meeting Scheduler](https://leetcode.com/problems/meeting-scheduler/)

## 6. Run-Length Encoded Sequence Merge

**Recognition:** Inputs represent repeated-value segments rather than individual elements.

**Core approach:** Consume the smaller remaining run, emit/merge the result segment, and advance exhausted runs.

- [Product of Two Run-Length Encoded Arrays](https://leetcode.com/problems/product-of-two-run-length-encoded-arrays/)

## 7. Fast/Slow Read-Write Pointers

**Recognition:** Modify an array in place while retaining valid elements or compressing runs.

**Core approach:** The read pointer scans input; the write pointer marks the next output position.

- [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- [Remove Duplicates From Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
- [Remove Duplicates From Sorted Array II](https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/)
- [String Compression](https://leetcode.com/problems/string-compression/)
- [Apply Operations to an Array](https://leetcode.com/problems/apply-operations-to-an-array/)

## 8. In-Place Partitioning

**Recognition:** Rearrange values according to parity, sign, or relation to a pivot.

**Core approach:** Move boundary pointers or write into separate logical regions while preserving required order.

- [Sort Array by Parity](https://leetcode.com/problems/sort-array-by-parity/)
- [Partition Array According to Given Pivot](https://leetcode.com/problems/partition-array-according-to-given-pivot/)
- [Rearrange Array Elements by Sign](https://leetcode.com/problems/rearrange-array-elements-by-sign/)

## 9. Sorted Two-Sum

**Recognition:** Find a pair satisfying an exact or upper-bound sum in sorted data.

**Core approach:** Increase the left pointer when the sum is too small; decrease the right pointer when it is too large.

- [Two Sum II — Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- [Two Sum Less Than K](https://leetcode.com/problems/two-sum-less-than-k/)

## 10. K-Sum after Sorting

**Recognition:** Find unique triplets/quadruplets or count tuples meeting a sum condition.

**Core approach:** Sort, fix leading values, reduce to two pointers, and skip duplicates carefully.

- [3Sum](https://leetcode.com/problems/3sum/)
- [4Sum](https://leetcode.com/problems/4sum/)
- [3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)

## 11. Two Pointers over Sorted Extremes

**Recognition:** Pair smallest and largest values to satisfy capacity, equality, or greedy score rules.

**Core approach:** Sort and decide whether the lightest/smallest can be paired with the heaviest/largest.

- [Assign Cookies](https://leetcode.com/problems/assign-cookies/)
- [Divide Players Into Teams of Equal Skill](https://leetcode.com/problems/divide-players-into-teams-of-equal-skill/)
- [Boats to Save People](https://leetcode.com/problems/boats-to-save-people/)
- [Bag of Tokens](https://leetcode.com/problems/bag-of-tokens/)

## 12. Two Ends for Transformed Sorted Output

**Recognition:** A monotonic transformation may reverse ordering around a turning point.

**Core approach:** Compare transformed values at both endpoints and fill output from the appropriate side.

- [Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)
- [Sort Transformed Array](https://leetcode.com/problems/sort-transformed-array/)

## 13. Opposite Ends for Maximum Area or Water

**Recognition:** The score depends on two boundaries and their distance.

**Core approach:** Evaluate both endpoints, then move the limiting boundary because keeping it cannot improve the result.

- [Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)

## 14. Sorted Min/Max Subsequences

**Recognition:** Count subsequences based only on their minimum and maximum values.

**Core approach:** Sort, move two pointers, and use powers of two to count all choices between valid endpoints.

- [Number of Subsequences That Satisfy the Given Sum Condition](https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/)

## 15. Array Rotation

**Recognition:** Shift an array cyclically in place.

**Core approach:** Use three reversals or cyclic replacement based on index mapping.

- [Rotate Array](https://leetcode.com/problems/rotate-array/)

## 16. Greedy Rearrangement

**Recognition:** Rearrange sorted values so local neighbors avoid a forbidden relationship.

**Core approach:** Sort and interleave values or swap adjacent positions to break monotonic triples.

- [Array With Elements Not Equal to Average of Neighbors](https://leetcode.com/problems/array-with-elements-not-equal-to-average-of-neighbors/)

## 17. Keep the Best Item in Each Adjacent Group

**Recognition:** Consecutive equal items conflict, and all but one must be removed at minimum cost.

**Core approach:** Scan each equal-color run, keeping its maximum removal cost and deleting the rest.

- [Minimum Time to Make Rope Colorful](https://leetcode.com/problems/minimum-time-to-make-rope-colorful/)

## 18. Recursive Index Mapping

**Recognition:** A position in a recursively generated sequence can be derived without constructing the sequence.

**Core approach:** Map the index to its parent position and track whether the symbol flips.

- [K-th Symbol in Grammar](https://leetcode.com/problems/k-th-symbol-in-grammar/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Compare or reverse from both ends | Opposite pointers |
| One deletion allowed in palindrome | Branch at first mismatch |
| Two logical strings | Parallel traversal |
| Merge sorted inputs | One pointer per input |
| Modify array in place | Read/write pointers |
| Group by pivot, sign, or parity | Partition pointers |
| Pair sum in sorted data | Left/right sum pointers |
| 3Sum or 4Sum | Sort + fix + two pointers |
| Pair lightest with heaviest | Greedy extremes |
| Transformed sorted values | Compare transformed endpoints |
| Area depends on two boundaries | Move limiting boundary |
| Remove from both string ends | Consume matching runs |

## Recommended Practice Order

1. Reverse String and Valid Palindrome
2. Move Zeroes and Remove Duplicates
3. Merge Sorted Array
4. Squares of a Sorted Array
5. Two Sum II
6. 3Sum and 4Sum
7. Container With Most Water
8. Boats to Save People
9. Trapping Rain Water
10. Parallel-string and RLE traversal
