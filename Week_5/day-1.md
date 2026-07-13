# Day 1

Problem: Search insert postion

leetcode link: https://leetcode.com/problems/search-insert-position/

Input: nums = [1,3,5,6], target = 5

Output: 2

Algorith: Check in the num of the index is the target if the target is not meet then return the index of the best place target should be


Python Solution:

```py
    def searchInsert(nums):
        best = 0
        big = -1
        for i, num in enumerate(nums):
            if num == target:
                return i
            if nums[i] - 1 == target:
                best = i
            elif nums[i] + 1 == target:
                best = i + 1
            if num > big:
                big = num
        if target > big:
            return len(nums)
        return best
```
