# Day 1

Problem: longestCommonPrefix

Input: s =Input: strs = ["bat","bag","bank","band"]

Output: "ba"

JavaScript Solution: 

```js
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
```

Python Solution:

```py
    def longestCommonPrefix(strs):
        output = ''
        text = ''
        for i in strs[0]:
            text += i
            if all(text in str for str in strs): # I wanted to use this method even if it not the most optimal
                output = text # checks if the current text is in all words
            else:
                return output
        return output
```
