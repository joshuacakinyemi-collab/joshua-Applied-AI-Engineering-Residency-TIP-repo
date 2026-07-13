# Day 1

Problem: Valid Anagram

Input: s = "racecar", t = "carrace"

Output: true

JavaScript Solution: 

```js
   isAnagram(s, t) { 
      if (s.split('').sort().join() === t.split('').sort().join()) { // turn string into an array, sort it, then turn it back in to string
        return true //check if the word is the same
      } else {
        return false
      }
    }
```

Python Solution:

```py
     def isAnagram(s, t):
        if sorted(s) == sorted(t): # learn how to sort in Python
            return True 
        else:
            return False
```


    longestCommonPrefix(strs) {
        let output = ''
        let str = ''
        for(let i = 0; i < strs[0].length; i++){ // loop the first word in the array
            str += strs[0][i] // add a letter from the first word
            for(let j = 0; j < strs.length; j++){ // loop the whole array
                if(!strs[j].includes(str)){ // if any of the word dosen't have the current string return the last word
                    return output
                }
            }
            output = str // makes the new string the return value
        }
        return output // if all is well just return
     }