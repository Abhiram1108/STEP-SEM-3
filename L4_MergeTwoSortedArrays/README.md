# L4. Merge Two Sorted Arrays

## Problem Description
Two class sections each submit their exam scores already sorted from lowest to highest. The examination office needs one single combined sorted list — without throwing both lists together and re-sorting everything from scratch.

## Task Requirements
- Accept two sorted integer arrays, `arr1` and `arr2`.
- Keep one index pointer for each array (`i` for `arr1`, `j` for `arr2`), both starting at 0, and create a new empty result array of size `arr1.length + arr2.length`.
- Using a `while` loop, repeatedly compare the current elements pointed to in `arr1` and `arr2`, copy the smaller one into the result array, and move that array's pointer forward by one.
- Once one array is fully copied over, copy all of the remaining elements from the other array directly onto the end of the result.
- Return the fully merged, fully sorted result array.

## Approach & Logic
- **Two-Pointer Merge Algorithm**:
  - Pointer `i` traverses `arr1`, pointer `j` traverses `arr2`, and pointer `k` traverses `result`.
  - In a `while (i < arr1.length && j < arr2.length)` loop, compare `arr1[i]` and `arr2[j]`. Append the smaller element to `result[k]` and increment the corresponding pointers.
  - Append any left-over elements from `arr1` or `arr2` using secondary `while` loops.

## Complexity
- **Time Complexity**: $\mathcal{O}(n + m)$ where $n$ and $m$ are lengths of `arr1` and `arr2`.
- **Space Complexity**: $\mathcal{O}(n + m)$ to store the merged output array.

## Sample Input & Output
| Input | Output |
| :--- | :--- |
| `arr1 = [1, 3, 5]`, `arr2 = [2, 4, 6]` | `[1, 2, 3, 4, 5, 6]` |
| `arr1 = []`, `arr2 = [1, 2, 3]` | `[1, 2, 3]` |

## How to Run
```bash
javac L4_MergeTwoSortedArrays/Solution.java
java L4_MergeTwoSortedArrays.Solution
```
