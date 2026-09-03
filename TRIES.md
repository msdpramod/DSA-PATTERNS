# Trie Problems Segregated by Pattern

Recommended order: **Trie basics → Prefix counting → Wildcards → Trie + DP → Trie + backtracking → Path tries → Autocomplete**.

> Each problem is placed under the Trie pattern most useful for recognizing its primary solution.

## 1. Basic Trie Operations

**Recognition:** Insert words and support exact-word or prefix queries.

**Core approach:** Each node stores child references and an end-of-word marker; traverse one character per level.

- [Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/)

## 2. Direct Prefix Counting

**Recognition:** Count how many words begin with a given prefix.

**Core approach:** Direct scanning is sufficient for one query; a Trie becomes useful for many repeated prefix queries.

- [Counting Words With a Given Prefix](https://leetcode.com/problems/counting-words-with-a-given-prefix/)

## 3. Prefix Frequency Aggregation

**Recognition:** Every word needs a score derived from how many words share each of its prefixes.

**Core approach:** Increment a pass count at each Trie node during insertion, then sum those counts while traversing every word.

- [Sum of Prefix Scores of Strings](https://leetcode.com/problems/sum-of-prefix-scores-of-strings/)

## 4. Prefix and Suffix Matching

**Recognition:** Count pairs where one word is both a prefix and suffix of another.

**Core approach:** For small constraints compare pairs directly; for scale, combine prefix and suffix characters into Trie states or use border hashing.

- [Count Prefix and Suffix Pairs I](https://leetcode.com/problems/count-prefix-and-suffix-pairs-i/)
- [Count Prefix and Suffix Pairs II](https://leetcode.com/problems/count-prefix-and-suffix-pairs-ii/)

## 5. Trie with Wildcard DFS

**Recognition:** Search patterns contain a wildcard that can represent any character.

**Core approach:** Follow a normal child for letters; on a wildcard, recursively try every child.

- [Design Add and Search Words Data Structure](https://leetcode.com/problems/design-add-and-search-words-data-structure/)

## 6. Trie + Dynamic Programming

**Recognition:** Segment a string using dictionary words while minimizing unmatched characters.

**Core approach:** From each position, walk forward through the Trie and combine valid word endings with suffix DP.

- [Extra Characters in a String](https://leetcode.com/problems/extra-characters-in-a-string/)

## 7. Trie + Grid Backtracking

**Recognition:** Search a board for many dictionary words simultaneously.

**Core approach:** Build one Trie for all words, DFS through the board, prune when the current path is not a Trie prefix, and deduplicate found words.

- [Word Search II](https://leetcode.com/problems/word-search-ii/)

## 8. Path Trie and Folder Filtering

**Recognition:** Hierarchical paths share slash-separated prefixes, or subfolders must be excluded.

**Core approach:** Treat path components as Trie edges, or sort paths so parent folders appear before their descendants.

- [Remove Sub-Folders From the Filesystem](https://leetcode.com/problems/remove-sub-folders-from-the-filesystem/)
- [Design File System](https://leetcode.com/problems/design-file-system/)

## 9. Hierarchical In-Memory File System

**Recognition:** Support directory creation, listing, file creation, appending, and reading over hierarchical paths.

**Core approach:** Model directories as Trie nodes whose children are path components; file nodes additionally store content.

- [Design In-Memory File System](https://leetcode.com/problems/design-in-memory-file-system/)

## 10. Trie + Ranked Suggestions

**Recognition:** Return the most frequent matching sentences after each typed prefix.

**Core approach:** Traverse the prefix Trie while maintaining ranked candidates at nodes or retrieving matching sentences with a heap.

- [Design Search Autocomplete System](https://leetcode.com/problems/design-search-autocomplete-system/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Insert, exact search, and starts-with | Basic Trie |
| Many prefix-count queries | Trie node pass counts |
| Wildcard characters | DFS from Trie node |
| Dictionary-based string segmentation | Trie + DP |
| Many words searched on one board | Trie + backtracking |
| Slash-separated hierarchy | Path-component Trie |
| Both prefix and suffix must match | Paired-character Trie or hashing |
| Ranked prefix suggestions | Trie + frequency ranking |

## Recommended Practice Order

1. Implement Trie
2. Counting Words With a Given Prefix
3. Sum of Prefix Scores
4. Add and Search Words
5. Extra Characters in a String
6. Word Search II
7. Remove Sub-Folders
8. File System designs
9. Prefix and Suffix Pairs II
10. Autocomplete System
