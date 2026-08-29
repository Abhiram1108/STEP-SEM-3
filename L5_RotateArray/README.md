# L5. Rotate Array

## Problem Description
A playlist needs to be shifted so the last few songs move to the front of the queue, rotating the whole list to the right by a given number of positions — solved the most direct way: work out exactly where every song lands, and build the new order from scratch.

## Task Requirements
- Accept an integer array `nums` and an integer `k`, the number of positions to rotate to the right.
- First reduce `k` using `k = k % nums.length` — rotating by the array's own length (or a multiple of it) has no visible effect.
- Create a new array of the same size. For every index `i` in the original array, work out its new position after rotation: `newArray[(i + k) % nums.length] = nums[i]`.
- Copy the values from the new array back into `nums` (or return the new array).

## Approach & Logic
- **Modulo Index Mapping**:
  - Calculate effective rotation `k = k % n`.
  - For each element at index `i`, place it into target index `(i + k) % n` in `newArray`.
  - Copy elements from `newArray` back into `nums`.

## Complexity
- **Time Complexity**: $\mathcal{O}(n)$ single pass to copy elements to new positions.
- **Space Complexity**: $\mathcal{O}(n)$ for the auxiliary array `newArray`.

## Sample Input & Output
| Input | Output | Explanation |
| :--- | :--- | :--- |
| `nums = [1, 2, 3, 4, 5, 6, 7]`, `k = 3` | `[5, 6, 7, 1, 2, 3, 4]` | Array shifted right by 3 positions |
| `nums = [1, 2]`, `k = 3` | `[2, 1]` | `k % length = 3 % 2 = 1`, single right rotation |

## How to Run
```bash
javac L5_RotateArray/Solution.java
java L5_RotateArray.Solution
```
