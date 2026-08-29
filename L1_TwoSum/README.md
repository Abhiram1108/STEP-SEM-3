# L1. Two Sum

## Problem Description
A shopkeeper wants to find two items from a list of prices that together add up to exactly a customer's budget. With only a handful of items on the shelf, the simplest approach — checking every possible pair — is more than fast enough.

## Task Requirements
- Accept an integer array `nums`, and an integer `target`.
- Using two nested loops, check every pair of different positions `(i, j)` in the array.
- If `nums[i] + nums[j]` equals `target`, return the two indices `[i, j]` immediately.
- Assume input always has exactly one valid pair, and cannot use the same element twice.

## Approach & Logic
- **Brute Force Pairwise Search**: Use an outer loop from index `i = 0` to `n - 1` and an inner loop from index `j = i + 1` to `n - 1`.
- For each pair, check if `nums[i] + nums[j] == target`.
- If a match is found, immediately return `new int[]{i, j}`.

## Complexity
- **Time Complexity**: $\mathcal{O}(n^2)$ due to nested for-loops checking all pairs.
- **Space Complexity**: $\mathcal{O}(1)$ auxiliary space as search is done in-place.

## Sample Input & Output
| Input | Output | Explanation |
| :--- | :--- | :--- |
| `nums = [2, 7, 11, 15]`, `target = 9` | `[0, 1]` | `nums[0] + nums[1] = 2 + 7 = 9` |
| `nums = [3, 2, 4]`, `target = 6` | `[1, 2]` | `nums[1] + nums[2] = 2 + 4 = 6` |

## How to Run
```bash
javac L1_TwoSum/Solution.java
java L1_TwoSum.Solution
```
