# Day 1

Problem: FizzBuzz

leetcode link: https://leetcode.com/problems/fizz-buzz/

```js
function fizzBuzz(n) {
  const result = [];
  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) {
      result.push('FizzBuzz');
    } else if (i % 3 === 0) {
      result.push('Fizz');
    } else if (i % 5 === 0) {
      result.push('Buzz');
    } else {
      result.push(String(i));
    }
  }
  return result;
}
```
Input: Input: n = 3

Output: Output: ["1","2","Fizz"]

Algorith: if n % 3 === 0 then place 'Fizz', if n % 5 === 0 then place 'Buzz', if nums can meet both condition then place 'FizzBuzz'


Python Solution:

```py
    def fizzBuzz(self, n):
        arr = []
    for i in range (1,n+1):
        if n % 15 == 0:
            arr.append('FizzBuzz')
        elif n % 5 == 0:
            arr.append('Buzz')
        elif n % 3 == 0:
            arr.append('Fizz')
        else:
            arr.append(str(i))

        return arr
```
