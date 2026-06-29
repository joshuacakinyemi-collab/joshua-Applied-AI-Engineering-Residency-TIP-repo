# Day 3

Problem:  4sum 2
leetcode link: https://leetcode.com/problems/4sum-ii/description/

Input: nums1 = [1,2], nums2 = [-2,-1], nums3 = [-1,2], nums4 = [0,2]

Output: 2

Algorith: check if the next elements after sets[num] has a num that is sets[num] + 1, keep going until that not true, check if it that length is the biggest, then replace the highest value. 

Python Solution:

```py
import math

    def longestConsecutive(self, nums: List[int]) -> int:
        num_set = set(nums)
        high = 0

        for num in num_set:
            if num - 1 not in num_set:
                length = 1
                while num + length in num_set:
                    length += 1
                high = max(high, length)

        return high
```