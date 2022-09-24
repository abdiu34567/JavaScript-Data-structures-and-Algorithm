## Primality Test

A primality test can be done by iterating from `2` to `n`, checking whether `modulus` division
(remainder) is equal to `zero`

```js
function isPrime(n) {
  if (n <= 1) {
    return false
  }

  for (var i = 2; i < n; i++) {
    if (n % i == 0) {
      return false
    }
  }

  return true
}
```

**Time Complexity: O(n)**

The time complexity is `O(n)` because this algorithm checks all numbers from `0 to n`.
This is an example of an algorithm that can be easily improved. Think about how this
method iterates through `2 to n`. Is it possible to find a pattern and make the algorithm
`faster?` First, any multiple of `2s` can be `ignored`, but there is more optimization possible.
Let’s list some prime numbers.

`2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97`

This is difficult to notice, but all primes are of the form `6k ± 1`, with the exception of
`2` and `3` where `k` is some integer. Here’s an example:

`5 = (6-1) , 7 = ((1*6) + 1), 13 = ((2*6) + 1)`

Also realize that for testing the prime number n, the loop only has to test until the
`square root` of n. This is because if the square root of n is not a prime number, n is not a
prime number by `mathematical definition`

```js
function isPrime(n) {
  if (n <= 1) return false
  if (n <= 3) return true
  // This is checked so that we can skip
  // middle five numbers in below loop
  if (n % 2 == 0 || n % 3 == 0) return false
  for (var i = 5; i * i <= n; i = i + 6) {
    if (n % i == 0 || n % (i + 2) == 0) return false
  }
  return true
}
```

**Time Complexity: O(sqrt(n))**

This improved solution cuts the time complexity down significantly
