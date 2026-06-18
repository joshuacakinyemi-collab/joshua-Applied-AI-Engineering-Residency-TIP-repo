# Day 2

Problem: Top k Frequent
leetcode link: https://leetcode.com/problems/top-k-frequent-elements/


Input: nums = [1,1,1,2,2,3], k = 2

Output: [1,2]

Algorith: Search the entire array for the k most frequent elements in the arr


Python Solution: 

```py
from collections import Counter
    def topKFrequent(nums):

        count = {}
        for item in nums:
            count[item] = count.get(item, 0) + 1
        
        sort = dict(sorted(count.items(), key=lambda item: item[1], reverse=True))
        
        arr = []
        for key in list(sort.keys())[:k]:
            
            arr.append(key)
        return arr 
```
