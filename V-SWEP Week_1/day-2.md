# Day 2

Problem: Contiguous Array
leetcode link: https://leetcode.com/problems/contiguous-array/description/


Input: nums = [0,1]

Output: 2

Algorith:

Python Solution: 

```py
    from collections import defaultdict
    def findMaxLength(nums):
        prefix = 0
        longest = 0

        first_seen = defaultdict(lambda: None)
        first_seen[0] = -1

        for i, num in enumerate(nums):
            if num == 1:
                prefix += 1
            else: prefix -= 1

            if first_seen[prefix] is not None:
                longest = max(longest, i - first_seen[prefix])
            else:
                first_seen[prefix] = i

        return longest
```
