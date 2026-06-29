# Day 4


Problem: Minimum Window Substring
leetcode link: https://leetcode.com/problems/minimum-window-substring/

Input: s = "ADOBECODEBANC", t = "ABC"

Output: "BANC"

Algorith: 

str = None
lets = t split into individual characters
// lets = ["A", "B", "C"]

// Outer loop: try every starting position in s
FOR i, index_letter IN enumerate(s):

new = index_letter // start the window at position i

// Inner loop: expand the window to the right from i
FOR j, moving IN enumerate(s):

new += moving  // keep growing the window

// Check if new contains every character in t
check = every letter in lets exists somewhere in new

IF check == True:

// Valid window found — is it the smallest so far?
IF str == None OR len(new) < len(str):
str = new

break // stop expanding, try next starting point

RETURN str

Python Solution:

```py
from collections import Counter

def minWindow(self, s: str, t: str) -> str:
        if not s or not t:
            return ""

        str = None
        need = Counter(t)
        for i in range(len(s)):
            new = ''
            have = Counter()
            for j in range(i, len(s)):
                new += s[j]
                have[s[j]] += 1
                check = all(have[letter] >= need[letter] for letter in need)

                if check:
                    if str is None or len(new) < len(str):
                        str = new
                    break
        return str if str is not None else ''


```