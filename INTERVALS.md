# Interval Problems Segregated by Pattern

Recommended order: **Basic traversal → Merge → Insert → Intersections → Greedy → Sweep line → Heap scheduling → Calendars → Dynamic intervals**.

> Some questions support several approaches. Each appears under the pattern most useful for recognizing it in an interview.

## 1. Gap and Range Traversal

**Recognition:** Sorted values or intervals are given; identify the uncovered portions between boundaries.

**Core approach:** Track the next expected value or merge coverage first, then emit each uncovered range.

- [Missing Ranges](https://leetcode.com/problems/missing-ranges/)
- [Count Days Without Meetings](https://leetcode.com/problems/count-days-without-meetings/)

## 2. Merge Overlapping Intervals

**Recognition:** Intervals may overlap and must be condensed into disjoint blocks.

**Core approach:** Sort by start time; extend the current end while intervals overlap.

- [Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- [Add Bold Tag in String](https://leetcode.com/problems/add-bold-tag-in-string/)
- [Employee Free Time](https://leetcode.com/problems/employee-free-time/)

## 3. Insert, Remove, and Split Intervals

**Recognition:** One interval is added to or removed from an existing disjoint interval list.

**Core approach:** Process intervals before, overlapping with, and after the target separately.

- [Insert Interval](https://leetcode.com/problems/insert-interval/)
- [Remove Interval](https://leetcode.com/problems/remove-interval/)

## 4. Two-List Interval Intersection

**Recognition:** Two sorted, disjoint interval lists must be compared.

**Core approach:** Use two pointers; emit the overlap, then advance the interval that finishes first.

- [Interval List Intersections](https://leetcode.com/problems/interval-list-intersections/)

## 5. Greedy Interval Selection

**Recognition:** Remove the fewest intervals, cover points with minimum resources, or retain maximum compatible intervals.

**Core approach:** Sort by end time and greedily preserve the interval that leaves the most room for future choices.

- [Non-Overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)
- [Minimum Number of Arrows to Burst Balloons](https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/)

## 6. Containment and Interval Ordering

**Recognition:** Determine whether intervals are fully covered or whether separated groups exist.

**Core approach:** Sort carefully by start and end; maintain the farthest covered endpoint.

- [Remove Covered Intervals](https://leetcode.com/problems/remove-covered-intervals/)
- [Check if Grid Can Be Cut into Sections](https://leetcode.com/problems/check-if-grid-can-be-cut-into-sections/)

## 7. Sweep Line and Event Counting

**Recognition:** Find the maximum number of simultaneously active intervals or whether overlap exceeds a limit.

**Core approach:** Convert each interval into start/end events or separately sort starts and ends.

- [Meeting Rooms](https://leetcode.com/problems/meeting-rooms/)
- [Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- [Divide Intervals Into Minimum Number of Groups](https://leetcode.com/problems/divide-intervals-into-minimum-number-of-groups/)
- [My Calendar II](https://leetcode.com/problems/my-calendar-ii/)

## 8. Heap-Based Resource Scheduling

**Recognition:** Assign rooms, chairs, or machines while reusing the earliest resource that becomes free.

**Core approach:** Sort arrivals; use one heap for active end times and, when identities matter, another for available resource IDs.

- [Meeting Rooms III](https://leetcode.com/problems/meeting-rooms-iii/)
- [The Number of the Smallest Unoccupied Chair](https://leetcode.com/problems/the-number-of-the-smallest-unoccupied-chair/)

## 9. Offline Queries with a Heap

**Recognition:** For every query point, find the best interval containing it.

**Core approach:** Sort intervals and queries; add eligible intervals to a heap and lazily remove expired ones.

- [Minimum Interval to Include Each Query](https://leetcode.com/problems/minimum-interval-to-include-each-query/)

## 10. Calendar Booking and Ordered Search

**Recognition:** Intervals arrive online and every new booking must be validated immediately.

**Core approach:** Use an ordered map/tree to inspect neighboring bookings, or use a balanced interval structure.

- [My Calendar I](https://leetcode.com/problems/my-calendar-i/)

## 11. Dynamic Disjoint Intervals

**Recognition:** Values arrive continuously and must be maintained as merged, non-overlapping ranges.

**Core approach:** Use an ordered map or Union-Find-style merging to join adjacent ranges.

- [Data Stream as Disjoint Intervals](https://leetcode.com/problems/data-stream-as-disjoint-intervals/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Find uncovered ranges | Gap traversal |
| Combine all overlaps | Sort + merge |
| Add/delete one range | Three-phase interval scan |
| Compare two sorted interval lists | Two pointers |
| Remove minimum overlaps | Greedy by end time |
| Count simultaneous intervals | Sweep line |
| Reuse rooms, chairs, or servers | Min-heap scheduling |
| Answer many point queries | Offline sorting + heap |
| Accept/reject bookings online | Ordered map/tree |
| Maintain ranges from a stream | Dynamic interval structure |

## Recommended Practice Order

1. Missing Ranges
2. Merge Intervals
3. Insert Interval
4. Interval List Intersections
5. Non-Overlapping Intervals
6. Meeting Rooms
7. Meeting Rooms II
8. Minimum Number of Arrows to Burst Balloons
9. Employee Free Time
10. Minimum Interval to Include Each Query
11. My Calendar I and II
12. Meeting Rooms III
13. Data Stream as Disjoint Intervals
