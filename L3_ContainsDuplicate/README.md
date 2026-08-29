# L3. Contains Duplicate

## Problem Description
Before finalizing an exam seating chart, the office must double-check that no roll number was accidentally entered twice in the list — by comparing every entry against every other entry.

## Task Requirements
- Accept an integer array `nums`.
- Using two nested loops, compare every element at position `i` against every element at a different position `j`.
- If any two different positions hold the exact same value, return `true` right away.
- If no matching pair is found after checking every possible pair, return `false`.

## Approach & Logic
- **Nested Loop Pairwise Comparison**:
  - Outer loop picks element at index `i`.
  - Inner loop checks elements at indices `j` where `j > i`.
  - If `nums[i] == nums[j]`, a duplicate exists -> return `true` immediately (early exit).
  - If both loops complete without matching elements, return `false`.

## Complexity
- **Time Complexity**: $\mathcal{O}(n^2)$ using nested loops to compare all distinct pairs.
- **Space Complexity**: $\mathcal{O}(1)$ auxiliary space.

## Sample Input & Output
| Input | Output | Explanation |
| :--- | :--- | :--- |
| `nums = [1, 2, 3, 1]` | `true` | The value 1 appears at two different positions |
| `nums = [1, 2, 3, 4]` | `false` | Every value is distinct |

## How to Run
```bash
javac L3_ContainsDuplicate/Solution.java
java L3_ContainsDuplicate.Solution
```
