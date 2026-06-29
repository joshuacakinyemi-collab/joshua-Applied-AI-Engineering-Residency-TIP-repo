# Day 2

Problem: Maximum Number of Vowels in a Substring of Given Length

leetcode link: https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/description/


Input: s = "abciiidef", k = 3

Output: 3

Algorith: 

have an array fill of vowel
make a variable n
make a loop for nums
    make a i varable
    have a while loop that goes as long i is not >= k
        take a k amount of letter and count the vowel
        if it more then n replace the value with k
        if n == k return k
return n


javaScript Solution:

Python Solution: 

```py
    def maxVowels(s):
        n = 0
        for i, num in enumerate(s):
            if n >= k:
                return n
            amount = 0
            j = 0
            while j <= k:
                add = j + i
                if add > len(s):
                    return n
                if s[add] == 'a' or s[add] == 'e' or s[add] == 'i' or s[add] == 'o' or s[add] == 'u':
                    amount += 1
                j += 1
            if amount > n:
                n = amount
        return n
```
