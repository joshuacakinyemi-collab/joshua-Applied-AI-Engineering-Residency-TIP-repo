# Day 1

Problem: Contains Duplicate

Input: nums = [1, 2, 3, 3]

Output: true

JavaScript Solution: 

```js
    hasDuplicate(nums) {
        let my_set = new Set() // O(1)
        for(let i = 0; i < nums.length; i++){ // O(n)
            if(!my_set.has(nums[i])) { // O(1)
                my_set.add(nums[i])
                continue;
            } else {
                return true
            }
        }
        return false
    }
```

