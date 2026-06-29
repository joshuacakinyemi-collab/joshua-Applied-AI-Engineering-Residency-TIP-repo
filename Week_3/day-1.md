# Day 1

Problem: Subarray Sum Equals K

leetcode link: https://leetcode.com/problems/subarray-sum-equals-k/description/

Input: nums = [1,1,1], k = 2

Output: 2

Algorith: Create an output array filled with 1s, as left pass for each index, store the product of everything to its left Right pass for each index, multiply what's already there by the product of everything to its right


Python Solution:

```py
    from collections import defaultdict
    def subarraySum(nums):
        prefixs = defaultdict(int)
        prefixs[0] = 1

        current_sum = 0
        count = 0

        for num in nums:
            current_sum += num

            complement = current_sum - k
            count += prefixs[complement]

            prefixs[current_sum] += 1

        return count
```
