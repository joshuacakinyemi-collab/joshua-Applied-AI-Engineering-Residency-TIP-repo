# Day 3

Problem:  Longest Consecutive Sequence
leetcode link: https://leetcode.com/problems/longest-consecutive-sequence/

Input: nums = [100,4,200,1,3,2]

Output: 4

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