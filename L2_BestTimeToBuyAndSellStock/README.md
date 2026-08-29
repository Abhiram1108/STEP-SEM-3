# L2. Best Time to Buy and Sell Stock

## Problem Description
A trainee investor has one week of daily stock prices and wants to know the single best day to buy and the single best later day to sell, to make the largest possible profit — found in one simple pass through the prices, left to right.

## Task Requirements
- Accept an integer array `prices`, where `prices[i]` is the price on day `i`.
- Walk through the array once, keeping track of the lowest price seen so far.
- At each day, work out the profit you'd make if you sold today: `today's price - lowest price seen so far`.
- Keep a running record of the largest such profit seen across the whole array.
- If the price only ever goes down, the answer is `0` — there's no profitable day to sell.

## Approach & Logic
- **Single-Pass Dynamic Tracking**:
  - Initialize `minPrice` to `prices[0]` and `maxProfit` to `0`.
  - Iterate through the array starting from index `1`.
  - Update `minPrice` if the current price is lower than `minPrice`.
  - Otherwise, compute potential profit `prices[i] - minPrice` and update `maxProfit` if this profit exceeds the current `maxProfit`.

## Complexity
- **Time Complexity**: $\mathcal{O}(n)$ because we iterate through the array only once.
- **Space Complexity**: $\mathcal{O}(1)$ auxiliary space.

## Sample Input & Output
| Input | Output | Explanation |
| :--- | :--- | :--- |
| `prices = [7, 1, 5, 3, 6, 4]` | `5` | Buy on day 2 at price 1, sell on day 5 at price 6 ($6 - 1 = 5$) |
| `prices = [7, 6, 4, 3, 1]` | `0` | Prices only fall, no profitable trade possible |

## How to Run
```bash
javac L2_BestTimeToBuyAndSellStock/Solution.java
java L2_BestTimeToBuyAndSellStock.Solution
```
