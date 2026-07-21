# Day 1

Problem: Majority Element

Input: nums = [5,5,1,1,1,5,5]

Output: 5


JavaScript Solution: 

```js
   majorityElement(nums) {
    let freq = {}
    let max = -Infinity
    let current

    for(let n of nums) { // O(n)
        freq[n] = (freq[n] || 0) + 1 // O(1)
        if (freq[n] > max) {
            max = freq[n]
            current = n
        }
    }

    return current
    }
```
