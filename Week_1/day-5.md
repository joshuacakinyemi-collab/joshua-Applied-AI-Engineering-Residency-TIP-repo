# Day 5

Problem: Palindrome Number
leetcode link: https://leetcode.com/problems/palindrome-number/description/

```js
function isPalindrome(x) {
  if (x < 0) return false;
  const str = x.toString();
  let left = 0;
  let right = str.length - 1;
  while (left < right) {
    if (str[left] !== str[right]) return false;
    left++;
    right--;
  }
  return true;
}
```
Input: x = 121

Output: true

Algorith: if the numbers can be look as the same then return true


Python Solution:

```py
def isPalindrome(x):
        if x < 0:
            return False
        s = str(x)
        left = 0
        right = len(s) - 1
        while left < right:
            if s[left] != s[right]:
                return False
            left+=1
            right-=1
        return True

```


Problem: 3Sum
leetcode link: https://leetcode.com/problems/3sum/description/

```js
function threeSum(nums) {
  const result = [];
  nums.sort((a, b) => a - b);
  for (let i = 0; i < nums.length - 2; i++) {
    if (i > 0 && nums[i] === nums[i - 1]) continue;
    let left = i + 1;
    let right = nums.length - 1;
    while (left < right) {
      const sum = nums[i] + nums[left] + nums[right];
      if (sum === 0) {
        result.push([nums[i], nums[left], nums[right]]);
        while (left < right && nums[left] === nums[left + 1]) left++;
        while (left < right && nums[right] === nums[right - 1]) right--;
        left++;
        right--;
      } else if (sum < 0) {
        left++;
      } else {
        right--;
      }
    }
  }
  return result;
}
```
Input: nums = [-1,0,1,2,-1,-4]

Output: [[-1,-1,2],[-1,0,1]]

Algorith: find the sum of all possibe triplet with any number totaling to 0.


Python Solution:

```py
def threeSum(nums):
result = []
        sort = sorted(nums)
        for i, num in enumerate(sort):
            if i > 0 and num == sort[i - 1]:
                continue
            left = i + 1
            right = len(sort) - 1
            while left < right:
                total = num + sort[left] + sort[right]
                if total == 0:
                    result.append([num, sort[left], sort[right]])
                    while left < right and sort[left] == sort[left + 1]:
                        left+=1
                    while left < right and sort[right] == sort[right - 1]: 
                        right-=1
                    left+=1
                    right-=1
                elif total < 0:
                    left+=1
                else:
                    right-=1
          return result

```