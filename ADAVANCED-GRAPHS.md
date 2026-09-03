# Advanced Graph Problems Segregated by Pattern

Recommended order: **Dijkstra → 0–1 BFS → Bellman–Ford → Floyd–Warshall → Topological sort → MST → Union-Find → Structural graph algorithms**.

> Some problems allow several solutions. Each appears under the pattern most useful for recognizing its intended or most instructive approach.

## 1. Standard Dijkstra — Minimum Additive Cost

**Recognition:** Edges have non-negative weights and the goal is minimum total distance or time.

**Core approach:** Store the best known distance for each node and process the smallest unsettled distance with a min-heap.

- [Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- [Minimum Cost to Convert String I](https://leetcode.com/problems/minimum-cost-to-convert-string-i/)

## 2. Minimax Path — Minimize the Maximum Edge or Cell

**Recognition:** Path cost is the largest effort, elevation, or time encountered rather than the sum.

**Core approach:** Use Dijkstra with `newCost = max(currentCost, edgeCost)`, or binary-search a feasible threshold.

- [Path With Minimum Effort](https://leetcode.com/problems/path-with-minimum-effort/)
- [Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/)

## 3. Maximin Path — Maximize the Minimum Safety

**Recognition:** A path's quality equals its weakest cell, and that minimum must be maximized.

**Core approach:** Compute cell safety first with multi-source BFS, then run maximum-capacity Dijkstra or binary search.

- [Find the Safest Path in a Grid](https://leetcode.com/problems/find-the-safest-path-in-a-grid/)

## 4. Maximum-Product Path

**Recognition:** Edge probabilities multiply and the path with the greatest product is required.

**Core approach:** Use a max-heap and relax neighbors by multiplying the current probability by the edge probability.

- [Path With Maximum Probability](https://leetcode.com/problems/path-with-maximum-probability/)

## 5. Grid Dijkstra with Special Constraints

**Recognition:** Grid moves have variable costs, waiting rules, or cell-specific arrival restrictions.

**Core approach:** Treat each cell as a weighted graph node and carefully derive the earliest valid neighbor arrival time.

- [Minimum Time to Visit a Cell in a Grid](https://leetcode.com/problems/minimum-time-to-visit-a-cell-in-a-grid/)

## 6. 0–1 BFS

**Recognition:** Every move costs exactly zero or one.

**Core approach:** Use a deque; push zero-cost transitions to the front and one-cost transitions to the back.

- [Minimum Obstacle Removal to Reach Corner](https://leetcode.com/problems/minimum-obstacle-removal-to-reach-corner/)
- [Minimum Cost to Make at Least One Valid Path in a Grid](https://leetcode.com/problems/minimum-cost-to-make-at-least-one-valid-path-in-a-grid/)

## 7. Multi-Source Boundary Expansion

**Recognition:** Heights or levels propagate inward from a boundary, and trapped volume depends on the lowest processed boundary.

**Core approach:** Add all boundary cells to a min-heap and expand inward while maintaining the effective boundary height.

- [Trapping Rain Water II](https://leetcode.com/problems/trapping-rain-water-ii/)

## 8. Shortest Path with Stop Constraints

**Recognition:** Minimize cost while using at most a fixed number of edges or stops.

**Core approach:** Use bounded Bellman–Ford, layered DP, or Dijkstra whose state includes stops used.

- [Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/)

## 9. All-Pairs Shortest Path

**Recognition:** Distances are needed between many or all pairs of nodes, usually with a small node count.

**Core approach:** Use Floyd–Warshall; each intermediate node progressively improves every source-destination pair.

- [Find the City With the Smallest Number of Neighbors at a Threshold Distance](https://leetcode.com/problems/find-the-city-with-the-smallest-number-of-neighbors-at-a-threshold-distance/)

## 10. Counting Shortest Paths

**Recognition:** Find both the shortest distance and how many distinct paths achieve it.

**Core approach:** During Dijkstra, replace the path count on a shorter route and add counts on an equal-length route.

- [Number of Ways to Arrive at Destination](https://leetcode.com/problems/number-of-ways-to-arrive-at-destination/)

## 11. Second-Shortest Path and Time-Dependent Edges

**Recognition:** The second distinct arrival time is required, and traversal may depend on traffic-light phases.

**Core approach:** Track the two best arrival times per node and incorporate waiting before each departure.

- [Second Minimum Time to Reach Destination](https://leetcode.com/problems/second-minimum-time-to-reach-destination/)

## 12. Topological Sort and Ordering Constraints

**Recognition:** Relative-order rules define a DAG, and a valid ordering or uniqueness must be determined.

**Core approach:** Build directed edges, compute indegrees, and process zero-indegree nodes with Kahn's algorithm.

- [Alien Dictionary](https://leetcode.com/problems/alien-dictionary/)
- [Sequence Reconstruction](https://leetcode.com/problems/sequence-reconstruction/)
- [Build a Matrix With Conditions](https://leetcode.com/problems/build-a-matrix-with-conditions/)

## 13. Eulerian Path

**Recognition:** Every directed edge or ticket must be used exactly once.

**Core approach:** Apply Hierholzer's algorithm; consume edges during DFS and append nodes after exhausting outgoing edges.

- [Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/)

## 14. Minimum Spanning Tree

**Recognition:** Connect every point or node with minimum total edge cost.

**Core approach:** Use Kruskal with Union-Find or Prim with a priority queue.

- [Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
- [Find Critical and Pseudo-Critical Edges in Minimum Spanning Tree](https://leetcode.com/problems/find-critical-and-pseudo-critical-edges-in-minimum-spanning-tree/)

## 15. Union-Find — Component Merging

**Recognition:** Edges progressively join components, and the result depends on component size, connectivity, or removable edges.

**Core approach:** Maintain parents, ranks/sizes, and component aggregates while processing edges in a useful order.

- [Making a Large Island](https://leetcode.com/problems/making-a-large-island/)
- [Minimum Cost Walk in Weighted Graph](https://leetcode.com/problems/minimum-cost-walk-in-weighted-graph/)
- [Number of Good Paths](https://leetcode.com/problems/number-of-good-paths/)
- [Remove Max Number of Edges to Keep Graph Fully Traversable](https://leetcode.com/problems/remove-max-number-of-edges-to-keep-graph-fully-traversable/)
- [Greatest Common Divisor Traversal](https://leetcode.com/problems/greatest-common-divisor-traversal/)

## 16. Functional Graph — Cycles with In-Trees

**Recognition:** Every node has exactly one outgoing edge.

**Core approach:** Peel acyclic nodes by indegree, analyze remaining cycles, and measure chains feeding into special cycles.

- [Maximum Employees to Be Invited to a Meeting](https://leetcode.com/problems/maximum-employees-to-be-invited-to-a-meeting/)

## 17. Articulation and Island Disconnection

**Recognition:** Determine whether removing a small number of vertices disconnects a graph or grid component.

**Core approach:** Use articulation-point logic, or exploit small constraints by removing each land cell and recounting components.

- [Minimum Number of Days to Disconnect Island](https://leetcode.com/problems/minimum-number-of-days-to-disconnect-island/)

## 18. Tree Diameter and Tree Merging

**Recognition:** Optimize the diameter after joining two trees.

**Core approach:** Find each tree's diameter with two BFS/DFS passes; connect their centers and compare resulting diameters.

- [Find Minimum Diameter After Merging Two Trees](https://leetcode.com/problems/find-minimum-diameter-after-merging-two-trees/)

## 19. Transformed Graph BFS

**Recognition:** The natural entities are groups, routes, or collections rather than individual locations.

**Core approach:** Build or traverse an implicit graph whose nodes represent the useful higher-level state.

- [Bus Routes](https://leetcode.com/problems/bus-routes/)

## 20. Bipartite Components and BFS Layering

**Recognition:** Nodes must be split into valid adjacent layers, maximizing the total number of layers across components.

**Core approach:** Check bipartiteness, then run BFS from candidate nodes to find the maximum layer count per component.

- [Divide Nodes Into the Maximum Number of Groups](https://leetcode.com/problems/divide-nodes-into-the-maximum-number-of-groups/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Minimum sum of non-negative weights | Dijkstra |
| Minimize the maximum edge/cell | Minimax Dijkstra |
| Maximize the weakest point | Maximin path |
| Probabilities multiply | Maximum-product Dijkstra |
| Edge costs are only 0 and 1 | 0–1 BFS |
| At most K edges/stops | Bellman–Ford or layered state |
| Distances between all pairs | Floyd–Warshall |
| Count optimal routes | Dijkstra + path counts |
| Need second distinct arrival | Two distances per node |
| Ordering or precedence constraints | Topological sort |
| Use every edge exactly once | Eulerian path |
| Connect everything at minimum cost | MST |
| Repeated component merging | Union-Find |
| Exactly one outgoing edge per node | Functional-graph decomposition |
| Removal disconnects a component | Articulation logic |
| Combine two trees optimally | Tree diameter and centers |
| Routes/groups are the useful states | Transformed graph BFS |

## Recommended Practice Order

1. Network Delay Time
2. Path With Minimum Effort
3. Swim in Rising Water
4. Path With Maximum Probability
5. 0–1 BFS grid problems
6. Cheapest Flights Within K Stops
7. Floyd–Warshall and shortest-path counting
8. Alien Dictionary and Sequence Reconstruction
9. Reconstruct Itinerary
10. Minimum Spanning Tree problems
11. Union-Find component problems
12. Functional graphs and articulation points
13. Tree diameter and transformed-state BFS
