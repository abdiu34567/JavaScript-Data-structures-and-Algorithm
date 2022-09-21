## Polynomial Rule : `Big-O to the Power of k`

The polynomial rule states that polynomial time complexities have a Big-O notation of
the `same` polynomial degree.

> `If f(n) is a polynomial of degree k, then f(n) is O(nk)`

```js
function a(n) {
  var count = 0
  for (var i = 0; i < n * n; i++) {
    count += 1 //line 4
  }
  return count
}
```

In this example, f(n) = **n<sup>2</sup>** because line 4 runs `n*n` iterations
