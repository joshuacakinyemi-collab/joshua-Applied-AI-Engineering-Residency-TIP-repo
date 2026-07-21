# Day 1

Problem: Valid Anagram

Input: s = "racecar", t = "carrace"

Output: true

JavaScript Solution: 

```js
    isAnagram(s, t) { 
      if (s.length !== t.length) return false; // O(1)
      const freq = {}; // O(1)

      for(let ch of s){ // O(n)
        freq[ch] = (freq[ch] || 0) + 1
      }

        for(let ch of t){ // O(M)
        freq[ch] = (freq[ch] || 0) - 1
      }

      for (let key in freq) { // O(1)
        if (freq[key] !== 0) {
          return false 
        }
      }
      return true
    }
```
