# Day 1

Problem: Running Sum of 1d Array

leetcode link: https://leetcode.com/problems/running-sum-of-1d-array/

Input: nums = [1,2,3,4]

Output: [1,3,6,10]

Algorith: 
make a sum variable that strt at 0
make a empty array
make a for loop
    and a element to sum
    add sum to the array
return array


Python Solution: 

```py
    def runningSum(nums):
        sum = 0
        arr = []

        for num in nums:
            sum += num
            arr.append(sum)
        return arr 
```