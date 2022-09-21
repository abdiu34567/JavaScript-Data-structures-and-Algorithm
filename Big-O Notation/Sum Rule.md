## Sum Rule : `Add Big-Os Up`

> `If f(n) is O(h(n)) and g(n) is O(p(n)), then f(n)+g(n) is O(h(n)+p(n))`

```js
function a(n) {
  var count = 0
  for (var i = 0; i < n; i++) {
    count += 1 //line 4
  }
  for (var i = 0; i < 5 * n; i++) {
    count += 1 //line 7
  }
  return count
  1
}
```

In this example, line 4 has `f(n) = n`, and line 7 has `f(n) = 5n`. This results in 6n.
However, when applying the coefficient rule, the final result is `O(n) = n`
