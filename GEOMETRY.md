# Math and Geometry Problems Segregated by Pattern

Recommended order: **Arithmetic → Number properties → GCD and primes → Matrix simulation → Geometry → Advanced math**.

> Some problems fit multiple categories. Each appears under the pattern most useful for recognizing its primary solution.

## 1. Direct Formula and Arithmetic

**Recognition:** The result follows from counting, parity, an arithmetic series, or a closed-form expression.

**Core approach:** Derive the formula before considering iteration.

- [Count Odd Numbers in an Interval Range](https://leetcode.com/problems/count-odd-numbers-in-an-interval-range/)
- [Calculate Money in Leetcode Bank](https://leetcode.com/problems/calculate-money-in-leetcode-bank/)
- [Count of Matches in Tournament](https://leetcode.com/problems/count-of-matches-in-tournament/)
- [Count Total Number of Colored Cells](https://leetcode.com/problems/count-total-number-of-colored-cells/)
- [Find Missing Observations](https://leetcode.com/problems/find-missing-observations/)
- [Distribute Candies Among Children II](https://leetcode.com/problems/distribute-candies-among-children-ii/)

## 2. GCD, Divisibility, and Factorization

**Recognition:** The problem involves common repetition, divisors, prime factors, or reducing a number through allowed factors.

**Core approach:** Use Euclid's algorithm, factorization, or divisibility invariants.

- [Greatest Common Divisor of Strings](https://leetcode.com/problems/greatest-common-divisor-of-strings/)
- [Insert Greatest Common Divisors in Linked List](https://leetcode.com/problems/insert-greatest-common-divisors-in-linked-list/)
- [Ugly Number](https://leetcode.com/problems/ugly-number/)
- [Minimum Factorization](https://leetcode.com/problems/minimum-factorization/)

## 3. Prime Numbers and Sieve

**Recognition:** Generate primes, test primality repeatedly, or select a prime under a constraint.

**Core approach:** Use the Sieve of Eratosthenes for a range; use trial division for isolated values.

- [Count Primes](https://leetcode.com/problems/count-primes/)
- [Closest Prime Numbers in Range](https://leetcode.com/problems/closest-prime-numbers-in-range/)
- [Prime Subtraction Operation](https://leetcode.com/problems/prime-subtraction-operation/)

## 4. Digit and Base Manipulation

**Recognition:** Process a number digit by digit, perform manual arithmetic, or convert between numeric representations.

**Core approach:** Use modulo/division or simulate the grade-school operation with carry.

- [Excel Sheet Column Title](https://leetcode.com/problems/excel-sheet-column-title/)
- [Largest Odd Number in String](https://leetcode.com/problems/largest-odd-number-in-string/)
- [Armstrong Number](https://leetcode.com/problems/armstrong-number/)
- [Plus One](https://leetcode.com/problems/plus-one/)
- [Palindrome Number](https://leetcode.com/problems/palindrome-number/)
- [Multiply Strings](https://leetcode.com/problems/multiply-strings/)
- [Integer to English Words](https://leetcode.com/problems/integer-to-english-words/)

## 5. Symbolic Number Conversion

**Recognition:** Convert between integers and a representation whose symbols have positional or subtractive rules.

**Core approach:** Scan symbols with local rules, or greedily subtract the largest representable value.

- [Roman to Integer](https://leetcode.com/problems/roman-to-integer/)
- [Integer to Roman](https://leetcode.com/problems/integer-to-roman/)

## 6. Powers and Exponentiation

**Recognition:** Compute large powers efficiently or determine whether a value can be expressed using powers.

**Core approach:** Use binary exponentiation, repeated division, or base-representation reasoning.

- [Power of Four](https://leetcode.com/problems/power-of-four/)
- [Pow(x, n)](https://leetcode.com/problems/powx-n/)
- [Check if Number Is a Sum of Powers of Three](https://leetcode.com/problems/check-if-number-is-a-sum-of-powers-of-three/)

## 7. Number-State Cycle Detection

**Recognition:** Repeatedly transform a number and determine whether the process terminates or loops.

**Core approach:** Store visited states or use Floyd's slow-and-fast pointer cycle detection.

- [Happy Number](https://leetcode.com/problems/happy-number/)

## 8. Matrix Traversal and Construction

**Recognition:** Visit or generate cells in a specific directional order.

**Core approach:** Maintain boundaries, direction vectors, or step lengths.

- [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
- [Spiral Matrix II](https://leetcode.com/problems/spiral-matrix-ii/)
- [Spiral Matrix III](https://leetcode.com/problems/spiral-matrix-iii/)
- [Spiral Matrix IV](https://leetcode.com/problems/spiral-matrix-iv/)

## 9. Matrix Transformation and Index Mapping

**Recognition:** Rotate, transpose, reshape, shift, or alter a matrix in place.

**Core approach:** Derive the source-to-destination index mapping; use marker rows/columns when extra space is restricted.

- [Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)
- [Rotate Image](https://leetcode.com/problems/rotate-image/)
- [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/)
- [Convert 1D Array Into 2D Array](https://leetcode.com/problems/convert-1d-array-into-2d-array/)
- [Shift 2D Grid](https://leetcode.com/problems/shift-2d-grid/)
- [Rotating the Box](https://leetcode.com/problems/rotating-the-box/)

## 10. Matrix Neighborhood and Validation

**Recognition:** Each answer depends on a cell's neighborhood, diagonals, row/column extrema, or a fixed-size subgrid.

**Core approach:** Enumerate only the relevant local cells or precompute row/column properties.

- [Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)
- [Image Smoother](https://leetcode.com/problems/image-smoother/)
- [Largest Local Values in a Matrix](https://leetcode.com/problems/largest-local-values-in-a-matrix/)
- [Lucky Numbers in a Matrix](https://leetcode.com/problems/lucky-numbers-in-a-matrix/)
- [Magic Squares in Grid](https://leetcode.com/problems/magic-squares-in-grid/)

## 11. Matrix Reordering and Median Optimization

**Recognition:** Rows/columns may be rearranged, or equalizing values requires minimum total movement.

**Core approach:** Sort frequency profiles; for absolute-distance minimization, target the median.

- [Largest Submatrix With Rearrangements](https://leetcode.com/problems/largest-submatrix-with-rearrangements/)
- [Minimum Operations to Make a Uni-Value Grid](https://leetcode.com/problems/minimum-operations-to-make-a-uni-value-grid/)
- [Best Meeting Point](https://leetcode.com/problems/best-meeting-point/)

## 12. Geometry — Slopes, Squares, and Reflection

**Recognition:** Points must form lines or shapes, or remain symmetric around an axis.

**Core approach:** Normalize slopes with GCD, count coordinate pairs, and use sets for reflected-point lookup.

- [Maximum Points on a Line](https://leetcode.com/problems/max-points-on-a-line/)
- [Detect Squares](https://leetcode.com/problems/detect-squares/)
- [Line Reflection](https://leetcode.com/problems/line-reflection/)
- [Widest Vertical Area Between Two Points Containing No Points](https://leetcode.com/problems/widest-vertical-area-between-two-points-containing-no-points/)

## 13. Simulation with Coordinates and Directions

**Recognition:** An object moves according to commands and orientation changes.

**Core approach:** Represent directions as vectors and simulate state transitions precisely.

- [Robot Bounded in Circle](https://leetcode.com/problems/robot-bounded-in-circle/)
- [Walking Robot Simulation](https://leetcode.com/problems/walking-robot-simulation/)

## 14. String and Sequence Simulation

**Recognition:** Count runs or place characters according to a repeating structural pattern.

**Core approach:** Track run lengths, row direction, or periodic positions.

- [Count Substrings with Only One Distinct Letter](https://leetcode.com/problems/count-substrings-with-only-one-distinct-letter/)
- [Zigzag Conversion](https://leetcode.com/problems/zigzag-conversion/)

## 15. Hashing and Combinatorial Counting

**Recognition:** Count equal products, repeated relationships, or arrangement frequencies.

**Core approach:** Store frequencies of a derived value and calculate how many valid combinations each collision creates.

- [Tuple with Same Product](https://leetcode.com/problems/tuple-with-same-product/)
- [Maximum Number of Ones](https://leetcode.com/problems/maximum-number-of-ones/)

## 16. Two Pointers and Sorted Numerical Search

**Recognition:** Find two numeric components satisfying a monotonic equation.

**Core approach:** Move pointers based on whether the current result is below or above the target.

- [Sum of Square Numbers](https://leetcode.com/problems/sum-of-square-numbers/)

## 17. Lexicographical Generation and Prefix Trees

**Recognition:** Numbers must be visited or selected in dictionary order without converting and sorting all strings.

**Core approach:** Treat decimal prefixes as an implicit 10-ary tree; count or traverse prefix subtrees.

- [Lexicographical Numbers](https://leetcode.com/problems/lexicographical-numbers/)
- [K-th Smallest in Lexicographical Order](https://leetcode.com/problems/k-th-smallest-in-lexicographical-order/)

## 18. Circular Elimination and Recurrence

**Recognition:** Elements are repeatedly removed around a circle.

**Core approach:** Use the Josephus recurrence or simulate with a queue when constraints are small.

- [Find the Winner of the Circular Game](https://leetcode.com/problems/find-the-winner-of-the-circular-game/)

## 19. Time and Modular Arithmetic

**Recognition:** Values wrap around a fixed cycle such as 24 hours.

**Core approach:** Convert to one unit, sort, and include the wraparound difference.

- [Minimum Time Difference](https://leetcode.com/problems/minimum-time-difference/)

## 20. Greedy Resource Exchange

**Recognition:** Consumed resources produce new resources under an exchange rule.

**Core approach:** Simulate exchanges or derive the total using quotient and remainder.

- [Water Bottles](https://leetcode.com/problems/water-bottles/)

## 21. Backtracking with Arithmetic Partitions

**Recognition:** Split digits into pieces whose numeric values must satisfy a target sum.

**Core approach:** Backtrack across split positions while pruning sums that exceed the target.

- [Find the Punishment Number of an Integer](https://leetcode.com/problems/find-the-punishment-number-of-an-integer/)

## 22. Restricted-API Deduction

**Recognition:** Direct access is unavailable; infer the answer through a comparison API.

**Core approach:** Establish a reference group and compare other indices against it.

- [Guess the Majority in a Hidden Array](https://leetcode.com/problems/guess-the-majority-in-a-hidden-array/)

## 23. Bitwise and Gray-Code Reasoning

**Recognition:** The operation flips bits under prefix or dependency constraints.

**Core approach:** Derive the Gray-code relationship or process bits from most significant to least significant.

- [Minimum Number of One Bit Operations to Make Integers Zero](https://leetcode.com/problems/minimum-one-bit-operations-to-make-integers-zero/)

## Pattern Selection Cheat Sheet

| Problem signal | Start with |
|---|---|
| Count from a predictable numeric pattern | Closed-form formula |
| Common divisor or repeated unit | GCD |
| Many prime queries in a range | Sieve |
| Manual numeric conversion | Digit simulation |
| Large exponent | Binary exponentiation |
| Repeated numerical transformation | Cycle detection |
| Spiral, rotation, reshape, or shift | Matrix index simulation |
| Points forming lines or shapes | Normalized geometry + hashing |
| Movement commands | Direction-vector simulation |
| Minimum total absolute distance | Median |
| Dictionary order of integers | Decimal prefix tree |
| Circular removals | Josephus recurrence |

## Recommended Practice Order

1. Direct formulas and digit manipulation
2. GCD, divisibility, and prime problems
3. Powers and number-state cycles
4. Matrix traversal
5. Matrix transformations
6. Matrix validation and optimization
7. Coordinate simulation
8. Geometry and hashing
9. Lexicographical prefix problems
10. Backtracking, restricted APIs, and bitwise math
