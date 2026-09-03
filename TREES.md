# Tree Problems Segregated by Pattern

Recommended order: **Traversal → Recursive properties → Paths → Level-order BFS → BSTs → Construction → LCA → Serialization → Tree DP**.

> Some problems fit several tree patterns. Each appears under the pattern most useful for deriving its primary recursive contract.

## 1. Fundamental DFS Traversals

**Recognition:** Visit every node in preorder, inorder, or postorder.

**Core approach:** Decide whether to process the node before, between, or after its children; know both recursive and iterative forms.

- [Binary Tree Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/)
- [Binary Tree Preorder Traversal](https://leetcode.com/problems/binary-tree-preorder-traversal/)
- [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/)
- [N-ary Tree Postorder Traversal](https://leetcode.com/problems/n-ary-tree-postorder-traversal/)

## 2. Recursive Tree Transformation

**Recognition:** Build a transformed copy or modify each subtree using the transformed children.

**Core approach:** Recursively transform left/right children, then attach or combine their results.

- [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- [Merge Two Binary Trees](https://leetcode.com/problems/merge-two-binary-trees/)
- [Clone N-ary Tree](https://leetcode.com/problems/clone-n-ary-tree/)

## 3. Height, Diameter, and Balance

**Recognition:** The answer depends on subtree heights or the longest path through a node.

**Core approach:** Return height from each subtree while updating a global diameter or validating height difference.

- [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
- [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- [Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/)
- [Diameter of N-ary Tree](https://leetcode.com/problems/diameter-of-n-ary-tree/)

## 4. Structural Comparison

**Recognition:** Determine whether two trees match exactly, contain one another, or match after allowed child swaps.

**Core approach:** Compare roots and recursively compare the required child pairings.

- [Same Tree](https://leetcode.com/problems/same-tree/)
- [Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/)
- [Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
- [Flip Equivalent Binary Trees](https://leetcode.com/problems/flip-equivalent-binary-trees/)

## 5. Root-to-Leaf Path State

**Recognition:** Accumulate a value or match a sequence along a root-to-leaf/downward path.

**Core approach:** Pass the running state downward and evaluate it at leaves or when the target sequence ends.

- [Path Sum](https://leetcode.com/problems/path-sum/)
- [Sum Root to Leaf Numbers](https://leetcode.com/problems/sum-root-to-leaf-numbers/)
- [Linked List in Binary Tree](https://leetcode.com/problems/linked-list-in-binary-tree/)

## 6. Postorder Subtree Aggregation

**Recognition:** Each node's answer depends on a summary returned by both children.

**Core approach:** Define exactly what DFS returns—count, sum, size, validity, best chain, or DP states—and combine postorder.

- [Evaluate Boolean Binary Tree](https://leetcode.com/problems/evaluate-boolean-binary-tree/)
- [Binary Tree Longest Consecutive Sequence](https://leetcode.com/problems/binary-tree-longest-consecutive-sequence/)
- [Binary Tree Longest Consecutive Sequence II](https://leetcode.com/problems/binary-tree-longest-consecutive-sequence-ii/)
- [Count Univalue Subtrees](https://leetcode.com/problems/count-univalue-subtrees/)
- [Maximum Average Subtree](https://leetcode.com/problems/maximum-average-subtree/)
- [Count Good Nodes in Binary Tree](https://leetcode.com/problems/count-good-nodes-in-binary-tree/)
- [Number of Good Leaf Nodes Pairs](https://leetcode.com/problems/number-of-good-leaf-nodes-pairs/)
- [Minimum Time to Collect All Apples in a Tree](https://leetcode.com/problems/minimum-time-to-collect-all-apples-in-a-tree/)

## 7. Tree DP — Take or Skip

**Recognition:** Selecting a node prevents selecting adjacent nodes.

**Core approach:** Return two values per node: best result when taking it and when skipping it.

- [House Robber III](https://leetcode.com/problems/house-robber-iii/)

## 8. BST Search and Pruning

**Recognition:** The BST ordering property can eliminate an entire subtree.

**Core approach:** Compare against the current value and recurse only into feasible branches.

- [Range Sum of BST](https://leetcode.com/problems/range-sum-of-bst/)
- [Closest Binary Search Tree Value](https://leetcode.com/problems/closest-binary-search-tree-value/)
- [Closest Binary Search Tree Value II](https://leetcode.com/problems/closest-binary-search-tree-value-ii/)

## 9. BST Validation and Inorder Ordering

**Recognition:** Validate ordering, find ranks, detect swapped nodes, or inspect adjacent sorted values.

**Core approach:** Use inorder traversal as a sorted stream or pass strict lower/upper bounds.

- [Verify Preorder Sequence in Binary Search Tree](https://leetcode.com/problems/verify-preorder-sequence-in-binary-search-tree/)
- [Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/)
- [Kth Smallest Element in a BST](https://leetcode.com/problems/kth-smallest-element-in-a-bst/)
- [Minimum Distance Between BST Nodes](https://leetcode.com/problems/minimum-distance-between-bst-nodes/)
- [Recover Binary Search Tree](https://leetcode.com/problems/recover-binary-search-tree/)
- [Largest BST Subtree](https://leetcode.com/problems/largest-bst-subtree/)

## 10. BST Construction and Mutation

**Recognition:** Build, insert, delete, or trim while preserving BST invariants.

**Core approach:** Recurse according to ordering; deletion replaces a two-child node with its successor or predecessor.

- [Convert Sorted Array to Binary Search Tree](https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/)
- [Insert into a Binary Search Tree](https://leetcode.com/problems/insert-into-a-binary-search-tree/)
- [Delete Node in a BST](https://leetcode.com/problems/delete-node-in-a-bst/)
- [Trim a Binary Search Tree](https://leetcode.com/problems/trim-a-binary-search-tree/)

## 11. Lowest Common Ancestor

**Recognition:** Find the lowest node whose subtree contains both targets.

**Core approach:** In a general tree, combine left/right search results; with parent pointers use two-pointer intersection; in a BST exploit ordering.

- [Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- [Lowest Common Ancestor of a Binary Tree III](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree-iii/)
- [Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)

## 12. Level-Order BFS

**Recognition:** The result is defined per depth, by visible side, or by horizontal position.

**Core approach:** Process one queue level at a time and retain the required node or aggregate from that level.

- [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- [Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/)
- [Binary Tree Zigzag Level Order Traversal](https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/)
- [Find Bottom Left Tree Value](https://leetcode.com/problems/find-bottom-left-tree-value/)
- [Reverse Odd Levels of Binary Tree](https://leetcode.com/problems/reverse-odd-levels-of-binary-tree/)
- [Minimum Number of Operations to Sort a Binary Tree by Level](https://leetcode.com/problems/minimum-number-of-operations-to-sort-a-binary-tree-by-level/)
- [Kth Largest Sum in a Binary Tree](https://leetcode.com/problems/kth-largest-sum-in-a-binary-tree/)
- [Cousins in Binary Tree II](https://leetcode.com/problems/cousins-in-binary-tree-ii/)
- [Check Completeness of a Binary Tree](https://leetcode.com/problems/check-completeness-of-a-binary-tree/)
- [Maximum Width of Binary Tree](https://leetcode.com/problems/maximum-width-of-binary-tree/)
- [Populating Next Right Pointers in Each Node](https://leetcode.com/problems/populating-next-right-pointers-in-each-node/)

## 13. Positional and Boundary Traversal

**Recognition:** Nodes are grouped by column, boundary role, or removal round.

**Core approach:** Carry positional metadata, split traversal by boundary type, or return height/removal round.

- [Binary Tree Vertical Order Traversal](https://leetcode.com/problems/binary-tree-vertical-order-traversal/)
- [Boundary of Binary Tree](https://leetcode.com/problems/boundary-of-binary-tree/)
- [Find Leaves of Binary Tree](https://leetcode.com/problems/find-leaves-of-binary-tree/)

## 14. Construct Tree from Traversals

**Recognition:** Rebuild a tree from preorder, inorder, or postorder sequences.

**Core approach:** Use traversal order to select the root and an index map to split the remaining ranges.

- [Construct Binary Tree From Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)
- [Construct Binary Tree From Inorder and Postorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-inorder-and-postorder-traversal/)
- [Construct Binary Tree From Preorder and Postorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-postorder-traversal/)

## 15. Construct or Identify Root from Relationships

**Recognition:** Parent-child descriptions or an unordered collection of nodes is given.

**Core approach:** Create nodes in a map and identify the one never appearing as a child; for node objects, use value/identity cancellation.

- [Create Binary Tree From Descriptions](https://leetcode.com/problems/create-binary-tree-from-descriptions/)
- [Find Root of N-Ary Tree](https://leetcode.com/problems/find-root-of-n-ary-tree/)

## 16. Serialization and Representation Conversion

**Recognition:** Convert trees to strings, between tree types, or into hierarchical region nodes.

**Core approach:** Define an unambiguous recursive encoding and matching decoder/constructor.

- [Construct String From Binary Tree](https://leetcode.com/problems/construct-string-from-binary-tree/)
- [Serialize and Deserialize N-ary Tree](https://leetcode.com/problems/serialize-and-deserialize-n-ary-tree/)
- [Encode N-ary Tree to Binary Tree](https://leetcode.com/problems/encode-n-ary-tree-to-binary-tree/)
- [Construct Quad Tree](https://leetcode.com/problems/construct-quad-tree/)

## 17. Subtree Serialization and Hashing

**Recognition:** Detect identical subtree structures appearing multiple times.

**Core approach:** Assign a canonical serialization or integer ID to each `(value,leftID,rightID)` tuple and count frequencies.

- [Find Duplicate Subtrees](https://leetcode.com/problems/find-duplicate-subtrees/)

## 18. Generate and Count Tree Structures

**Recognition:** Count or explicitly generate every structurally distinct tree.

**Core approach:** Choose each valid root or subtree-size split, then combine all left and right possibilities with memoization.

- [Unique Binary Search Trees](https://leetcode.com/problems/unique-binary-search-trees/)
- [Unique Binary Search Trees II](https://leetcode.com/problems/unique-binary-search-trees-ii/)
- [All Possible Full Binary Trees](https://leetcode.com/problems/all-possible-full-binary-trees/)

## 19. Compare Derived Tree Sequences

**Recognition:** Two trees are compared through their leaf order or sorted value streams.

**Core approach:** Generate the needed sequences lazily or eagerly, then compare with pointers/iterators.

- [Leaf-Similar Trees](https://leetcode.com/problems/leaf-similar-trees/)
- [Two Sum BSTs](https://leetcode.com/problems/two-sum-bsts/)

## 20. Nested Hierarchy Traversal

**Recognition:** The input is a recursively nested list rather than an explicit tree node structure.

**Core approach:** Traverse by depth; for inverse weighting, aggregate level sums cumulatively.

- [Nested List Weight Sum II](https://leetcode.com/problems/nested-list-weight-sum-ii/)

## 21. Organizational Tree and Propagation

**Recognition:** Employees or entities form a parent-child hierarchy, and actions/times propagate through descendants.

**Core approach:** Build children lists and DFS/BFS from the root while carrying time or checking ancestor/descendant state.

- [Time Needed to Inform All Employees](https://leetcode.com/problems/time-needed-to-inform-all-employees/)
- [Operations on Tree](https://leetcode.com/problems/operations-on-tree/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Visit nodes in a specific order | DFS traversal |
| Longest path or balanced height | Postorder height |
| Compare two tree structures | Paired recursion |
| Accumulate along root-to-leaf path | Downward state |
| Aggregate child summaries | Postorder contract |
| Choose non-adjacent nodes | Take/skip tree DP |
| Search or prune by value | BST ordering |
| Rank or adjacent BST values | Inorder traversal |
| Result grouped by depth | Level-order BFS |
| Rebuild from traversal arrays | Root selection + index ranges |
| Find shared ancestor | LCA |
| Detect repeated structures | Subtree hashing |
| Generate all tree shapes | Recursive combinations + memoization |

## Recommended Practice Order

1. Preorder, inorder, and postorder
2. Maximum Depth, Invert Tree, and Same Tree
3. Diameter and Balanced Tree
4. Path Sum and subtree aggregation
5. Level Order and Right Side View
6. BST validation, search, and k-th smallest
7. LCA variants
8. Tree construction from traversals
9. Serialization and structural hashing
10. Tree DP and generated-tree problems
