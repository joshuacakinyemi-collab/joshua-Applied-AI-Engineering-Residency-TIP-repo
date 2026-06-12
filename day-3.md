# Day 3

Problem: 
leetcode link:

```js
function reverseString(s) {
  let left = 0;
  let right = s.length - 1;
  while (left < right) {
    let temp = s[left];
    s[left] = s[right];
    s[right] = temp;
    left++;
    right--;
  }
  return s;
}
```
Input: s = ["h","e","l","l","o"]

Output: ["o","l","l","e","h"]

Algorith: Have two variables array, with left staring as 0, and right being the last placement of the array.take the element from the left position and swap it with the element from the right position, then increments left, and decrements right.


Python Solution:

```py
def reverseString(s):
        left = 0
        right = len(s) - 1
        while left < right:
            temp = s[left]
            s[left] = s[right]
            s[right] = temp
            left += 1
            right -= 1
            print(left)
        return s

```


Problem: Longest Substring Without Repeating Characters
leetcode link: https://leetcode.com/problems/longest-substring-without-repeating-characters/description/

```js
function lengthOfLongestSubstring(s) {
  let seen = {};
  let left = 0;
  let maxLength = 0;
  for (let right = 0; right < s.length; right++) {
    if (seen[s[right]] !== undefined && seen[s[right]] >= left) {
      left = seen[s[right]] + 1;
    }
    seen[s[right]] = right;
    maxLength = Math.max(maxLength, right - left + 1);
  }
  return maxLength;
}
```
Input: s = "abcabcbb"

Output: 3

Algorith: The str length that can only go up to  3 since the rest of the letter are the same letter.


Python Solution:

```py
def lengthOfLongestSubstring(s):
      seen = {}
      left = 0
      maxLength = 0
      for i, str in enumerate(s):
          if str in seen and seen[str] >= left:
              left = seen[str] + 1
          seen[str] = i
          maxLength = max(maxLength, i - left + 1)
      return maxLength

```