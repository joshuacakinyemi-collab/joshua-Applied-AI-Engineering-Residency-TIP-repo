# Day 1

Problem: product-of-array-except-self

leetcode link: https://leetcode.com/problems/product-of-array-except-self/

Input: nums = [1,2,3,4]

Output: [24,12,8,6]

Algorith: Create an output array filled with 1s, as left pass for each index, store the product of everything to its left Right pass for each index, multiply what's already there by the product of everything to its right


Python Solution:

```py
    def productExceptSelf(nums):
        arr = [1]
        left = 1
        right = 14
        for i in range(1, len(nums)):
            left = nums[i - 1] * left
            arr.append(left)

        for i in range(len(nums) - 2, -1, -1):
            right = nums[i + 1] * right
            arr[i] = right * arr[i]

        return arr
```
