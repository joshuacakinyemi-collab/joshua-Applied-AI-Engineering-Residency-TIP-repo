# Day 1

Problem: twoSum

Input: nums = [3,4,5,6], target = 7

Output: [0,1]

JavaScript Solution: 

```js
    twoSum(nums, target) {
        for(let i = 0; i < nums.length; i++) { // first loop track the first index
            for(let j = i+1; j < nums.length; j++){ // second loop track all possible sum with the first index
                if(nums[i] + nums[j] === target){ // if the two sum equal to the target the return the two index
                    return [i,j]
                }
            }
        }
    }
```

Python Solution:

```py
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i, inum in enumerate(nums):
            for j, jnum in enumerate(nums):
                if i == j: # need to add guard clause to prevent the index being the same
                    continue
                if inum + jnum == target:
                    return [i,j]
```
