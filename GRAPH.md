# Graph Problems Segregated by Pattern

Recommended order: **Grid DFS/BFS → Graph Traversal → Multi-Source BFS → Topological Sort → Union-Find → Shortest Path → Advanced Graphs**.

> Some problems fit multiple patterns. Each appears under its clearest primary solution.

## 1. Grid DFS/BFS — Flood Fill and Islands

**Recognition:** Explore neighboring cells in a matrix.

- [Island Perimeter](https://leetcode.com/problems/island-perimeter/)
- [Flood Fill](https://leetcode.com/problems/flood-fill/)
- [Number of Islands](https://leetcode.com/problems/number-of-islands/)
- [Max Area of Island](https://leetcode.com/problems/max-area-of-island/)
- [Maximum Number of Fish in a Grid](https://leetcode.com/problems/maximum-number-of-fish-in-a-grid/)
- [Number of Distinct Islands](https://leetcode.com/problems/number-of-distinct-islands/)
- [Number of Distinct Islands II](https://leetcode.com/problems/number-of-distinct-islands-ii/)
- [Path with Maximum Gold](https://leetcode.com/problems/path-with-maximum-gold/)
- [Check if Move Is Legal](https://leetcode.com/problems/check-if-move-is-legal/)

## 2. Boundary DFS/BFS — Regions and Enclaves

**Recognition:** Start from the boundary, compare two grids, or find enclosed regions.

- [Count Sub Islands](https://leetcode.com/problems/count-sub-islands/)
- [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/)
- [Surrounded Regions](https://leetcode.com/problems/surrounded-regions/)
- [Number of Closed Islands](https://leetcode.com/problems/number-of-closed-islands/)
- [Number of Enclaves](https://leetcode.com/problems/number-of-enclaves/)

## 3. Basic Graph DFS/BFS — Reachability and Components

**Recognition:** Build an adjacency list, mark visited nodes, and traverse components.

- [Clone Graph](https://leetcode.com/problems/clone-graph/)
- [Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)
- [Number of Provinces](https://leetcode.com/problems/number-of-provinces/)
- [Count the Number of Complete Components](https://leetcode.com/problems/count-the-number-of-complete-components/)
- [Detonate the Maximum Bombs](https://leetcode.com/problems/detonate-the-maximum-bombs/)
- [Web Crawler](https://leetcode.com/problems/web-crawler/)
- [Nested List Weight Sum](https://leetcode.com/problems/nested-list-weight-sum/)

## 4. Multi-Source BFS — Distance or Spread

**Recognition:** Several sources spread simultaneously, or cells need the nearest-source distance.

- [Walls and Gates](https://leetcode.com/problems/walls-and-gates/)
- [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)
- [As Far from Land as Possible](https://leetcode.com/problems/as-far-from-land-as-possible/)
- [Shortest Distance from All Buildings](https://leetcode.com/problems/shortest-distance-from-all-buildings/)
- [Maximum Number of Points From Grid Queries](https://leetcode.com/problems/maximum-number-of-points-from-grid-queries/)

## 5. Unweighted Shortest Path — Level-Order BFS

**Recognition:** Every move has equal cost; the first BFS arrival is optimal.

- [Snakes and Ladders](https://leetcode.com/problems/snakes-and-ladders/)
- [Open the Lock](https://leetcode.com/problems/open-the-lock/)
- [Shortest Bridge](https://leetcode.com/problems/shortest-bridge/)
- [Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
- [Shortest Path with Alternating Colors](https://leetcode.com/problems/shortest-path-with-alternating-colors/)
- [Minimum Knight Moves](https://leetcode.com/problems/minimum-knight-moves/)
- [Word Ladder](https://leetcode.com/problems/word-ladder/)
- [Shortest Distance After Road Addition Queries I](https://leetcode.com/problems/shortest-distance-after-road-addition-queries-i/)

## 6. Implicit-State Graphs

**Recognition:** Board positions, puzzle arrangements, or game states act as nodes.

- [Sliding Puzzle](https://leetcode.com/problems/sliding-puzzle/)
- [The Maze](https://leetcode.com/problems/the-maze/)
- [The Maze III](https://leetcode.com/problems/the-maze-iii/)
- [Minimum Number of Days to Eat N Oranges](https://leetcode.com/problems/minimum-number-of-days-to-eat-n-oranges/)

## 7. Weighted Shortest Path

**Recognition:** Moves have different non-negative costs; use Dijkstra or a priority queue.

- [The Maze II](https://leetcode.com/problems/the-maze-ii/)
- [Evaluate Division](https://leetcode.com/problems/evaluate-division/)

## 8. Topological Sort — Dependencies and DAGs

**Recognition:** Prerequisites, recipes, or tasks must be processed in a valid order.

- [Course Schedule](https://leetcode.com/problems/course-schedule/)
- [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- [Course Schedule IV](https://leetcode.com/problems/course-schedule-iv/)
- [Find All Possible Recipes from Given Supplies](https://leetcode.com/problems/find-all-possible-recipes-from-given-supplies/)
- [Parallel Courses](https://leetcode.com/problems/parallel-courses/)
- [Parallel Courses III](https://leetcode.com/problems/parallel-courses-iii/)
- [Largest Color Value in a Directed Graph](https://leetcode.com/problems/largest-color-value-in-a-directed-graph/)

## 9. Directed Graphs — Cycles, Safety, and Reachability

**Recognition:** Edge direction matters; detect cycles, safe nodes, or valid routes.

- [Find Champion II](https://leetcode.com/problems/find-champion-ii/)
- [Find Eventual Safe States](https://leetcode.com/problems/find-eventual-safe-states/)
- [All Paths from Source Lead to Destination](https://leetcode.com/problems/all-paths-from-source-lead-to-destination/)
- [Minimum Number of Vertices to Reach All Nodes](https://leetcode.com/problems/minimum-number-of-vertices-to-reach-all-nodes/)
- [Find Closest Node to Given Two Nodes](https://leetcode.com/problems/find-closest-node-to-given-two-nodes/)

## 10. Union-Find — Connectivity and Merging

**Recognition:** Repeatedly connect nodes, merge groups, or detect redundant edges.

- [Graph Valid Tree](https://leetcode.com/problems/graph-valid-tree/)
- [Redundant Connection](https://leetcode.com/problems/redundant-connection/)
- [Accounts Merge](https://leetcode.com/problems/accounts-merge/)
- [Regions Cut by Slashes](https://leetcode.com/problems/regions-cut-by-slashes/)
- [Number of Islands II](https://leetcode.com/problems/number-of-islands-ii/)
- [Sentence Similarity II](https://leetcode.com/problems/sentence-similarity-ii/)
- [Find All People With Secret](https://leetcode.com/problems/find-all-people-with-secret/)

## 11. Tree Graphs — DFS, Rerooting, and Leaf Trimming

**Recognition:** There is a unique path between every pair of nodes.

- [Reorder Routes to Make All Paths Lead to the City Zero](https://leetcode.com/problems/reorder-routes-to-make-all-paths-lead-to-the-city-zero/)
- [Minimum Fuel Cost to Report to the Capital](https://leetcode.com/problems/minimum-fuel-cost-to-report-to-the-capital/)
- [Minimum Score of a Path Between Two Cities](https://leetcode.com/problems/minimum-score-of-a-path-between-two-cities/)
- [Minimum Height Trees](https://leetcode.com/problems/minimum-height-trees/)
- [Most Profitable Path in a Tree](https://leetcode.com/problems/most-profitable-path-in-a-tree/)
- [Kill Process](https://leetcode.com/problems/kill-process/)
- [Maximum Number of K-Divisible Components](https://leetcode.com/problems/maximum-number-of-k-divisible-components/)

## 12. Coloring and Structural Validation

**Recognition:** Assign groups/colors or validate ordering relationships.

- [Is Graph Bipartite?](https://leetcode.com/problems/is-graph-bipartite/)
- [Verifying an Alien Dictionary](https://leetcode.com/problems/verifying-an-alien-dictionary/)

## 13. Degree Counting and Universal Nodes

**Recognition:** Incoming/outgoing degree reveals the answer without full traversal.

- [Find the Town Judge](https://leetcode.com/problems/find-the-town-judge/)
- [Find the Celebrity](https://leetcode.com/problems/find-the-celebrity/)
- [Count Servers that Communicate](https://leetcode.com/problems/count-servers-that-communicate/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Connected cells, islands, or colors | Grid DFS/BFS |
| Regions touching/not touching an edge | Boundary DFS/BFS |
| Nearest source or simultaneous spread | Multi-source BFS |
| Minimum equal-cost moves | BFS |
| Minimum weighted cost | Dijkstra |
| Prerequisites or dependency order | Topological sort |
| Repeated merging/connectivity queries | Union-Find |
| Two incompatible groups | Bipartite coloring |
| Unique path between node pairs | Tree DFS |
| Puzzle configurations/generated moves | Implicit-state graph |

## Recommended Practice Order

1. Grid DFS/BFS
2. Basic graph traversal
3. Multi-source and shortest-path BFS
4. Topological sort
5. Union-Find
6. Directed-graph reasoning
7. Tree graphs
8. Dijkstra and specialized graph problems
