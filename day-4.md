# Day 4

Problem: containsDuplicate
leetcode link: https://leetcode.com/problems/contains-duplicate/description/

```js
function containsDuplicate(nums) {
  const seen = new Set();
  for (let i = 0; i < nums.length; i++) {
    if (seen.has(nums[i])) {
      return true;
    }
    seen.add(nums[i]);
  }
  return false;
}
```
Input: nums = [1,2,3,1]

Output: true

Algorith: if a value in a array contain a copy then return true, else return false.


Python Solution:

```py
def containsDuplicate(nums):
        seen = set()
        for item in nums:
            if item in seen: 
                return True
            else:
                seen.add(item)
        return False

```

Problem: Group Anagrams
leetcode link: https://leetcode.com/problems/group-anagrams/submissions/2029860577/

```js
function groupAnagrams(strs) {
  const map = {};
  for (let i = 0; i < strs.length; i++) {
    const key = strs[i].split('').sort().join('');
    if (map[key] === undefined) {
      map[key] = [];
    }
    map[key].push(strs[i]);
  }
  return Object.values(map);
}
```
Input: strs = ["eat","tea","tan","ate","nat","bat"]

Output: [["bat"],["nat","tan"],["ate","eat","tea"]]

Algorith: by sorting each value, we'll place strings into smaller array the contains the same same exact letter


Python Solution:

```py
def groupAnagrams(strs):
    map = {}
    for str in strs:
    key = str.split().sort().join()
    if map[key] === None:
      map[key] = []
    
    map[key].append(str)
  
  return map.values()

```
