# Day 2

Problem: twoSum
leetcode link: https://leetcode.com/problems/two-sum/

```js
function twoSum(nums, target) {
  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      if (nums[i] + nums[j] === target) {
        return [i, j];
      }
    }
  }
}
```
Input: [2,7,11,15], 9

Output: [0,1]

Algorith: check for the first two number the equal to the target value


Python Solution: 

```py
def twoSum(prices, target):
for i, val_i in enumerate(nums):
    for j, val_j in enumerate(nums):
        if i != j and val_i + val_j == target: 
          return [i, j]   
```

Problem: Best Time to Buy and Sell Stock
leetcode link: https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/

```js
function maxProfit(prices) {
  let minPrice = Infinity;
  let maxProfit = 0;
  for (let i = 0; i < prices.length; i++) {
    if (prices[i] < minPrice) {
      minPrice = prices[i];
    } else if (prices[i] - minPrice > maxProfit) {
      maxProfit = prices[i] - minPrice;
    }
  }
  return maxProfit;
}
```
Input: [7,1,5,3,6,4]

Output: 5

Algorith: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.


Python Solution:

```py
def maxProfit(prices):
  minPrice = inf
  maxProfit = 0
    for i, val_i in enumerate(nums):
      if val_i < minPrice:
        minPrice = val_i
      elif val_i - minPrice > maxProfit:
        maxProfit = val_i - minPrice
    return maxProfit;
```