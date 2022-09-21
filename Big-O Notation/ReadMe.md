## Big-O Notation

The Big-O notation measures the `worst-case complexity` of an algorithm In Big-O notation, `n` represents the number of inputs

The question asked with Big-O is the following: `“What will happen as n approaches infinity?”`

When you implement an algorithm, Big-O notation is important because it tells you how efficient the algorithm is and analyze an implementation of an algorithm with respect to both `time` (execution time) and `space` (memory consumed)

## Examples

`O(1)` does not change with respect to input space. Hence, O(1) is referred to as being
`constant time`

An example of an O(1) algorithm is accessing an item in the `array` by its
`index`

O(n) is linear time and applies to algorithms that must do `n` operations in the
`worst-case scenario`

An example of an `O(n)` algorithm is printing numbers from `0 to n-1`

```js
function Linear(n) {
  for (var i = 0; i < n; i++) {
    console.log(i)
  }
}
```

Similarly, `O(n2)` is quadratic time

```js
function Quadratic(n) {
  for (var i = 0; i < n; i++) {
    console.log(i)

    for (var j = i; j < n; j++) {
      console.log(j)
    }
  }
}
```

`O(n3)` is cubic time

```js
function Cubic(n) {
  for (var i = 0; i < n; i++) {
    console.log(i)

    for (var j = i; j < n; j++) {
      console.log(j)

      for (var k = j; j < n; j++) {
        console.log(k)
      }
    }
  }
}
```
