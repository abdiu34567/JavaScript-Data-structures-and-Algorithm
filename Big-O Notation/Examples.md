## Examples

**❇️ Calculating Time complexity**

```js
function someFunction(n) {
  for (var i = 0; i < n * 1000; i++) {
    for (var j = 0; j < n * 20; j++) {
      console.log(i + j)
    }
  }
}
```

- **O(n<sup>2</sup>)**
- _There are two nested loops. Ignore the constants in front of n_

```js
function someFunction(n) {
  for (var i = 0; i < n; i++) {
    for (var j = 0; j < n; j++) {
      for (var k = 0; k < n; k++) {
        for (var l = 0; l < 10; l++) {
          console.log(i + j + k + l)
        }
      }
    }
  }
}
```

- **O(n<sup>3</sup>)**
- _There are four nested loops, but the last loop runs only until 10_

```js
function someFunction(n) {
  for (var i = 0; i < 1000; i++) {
    console.log('hi')
  }
}
```

- **O(1)**
- _Constant complexity. The function runs from 0 to 1000. This does not depend on n_

```js
function someFunction(n) {
  for (var i = 0; i < n * 10; i++) {
    console.log(n)
  }
}
```

- **O(n)**
- _Linear complexity. The function runs from 0 to 10n. Constants are ignored in Big-O_

```js
function someFunction(n) {
  for (var i = 0; i < n; i * 2) {
    console.log(n)
  }
}
```

- **O(log<sub>2</sub><sup>n</sup>)**
- _Logarithmic complexity. For a given `n`, this will operate only log<sub>2</sub><sup>n</sup> times because `i` is incremented by multiplying by 2 rather than adding 1 as in the other examples_

```js
function someFunction(n) {
  while (true) {
    console.log(n)
  }
}
```

- **O(∞)**
- _Infinite loop. This function will not end_
