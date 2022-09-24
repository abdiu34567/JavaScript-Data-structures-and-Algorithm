## **Number.EPSILON**

The Number.EPSILON property represents the difference between `1` and the `smallest floating` point number `greater than 1`

> `This is useful for the problem with floating-point approximation`

```js
function numberEquals(x, y) {
  return Math.abs(x - y) < Number.EPSILON
}

numberEquals(0.1 + 0.2, 0.3) // true
```

However, `Number.EPSILON` is inappropriate for any arithmetic operating on a `larger magnitude`. If your data is on the **10<sup>3</sup>** order of magnitude, the decimal part will have a much `smaller` accuracy than Number.EPSILON:

```js
function equal(x, y) {
  return Math.abs(x - y) < Number.EPSILON
}

const x = 1000.1
const y = 1000.2
const z = 2000.3
console.log(x + y) // 2000.3000000000002; error of 10^-13 instead of 10^-16
console.log(equal(x + y, z)) // false
```

In this case, a larger `tolerance` is required. As the numbers compared have a magnitude of approximately 2000, a multiplier such as `2000 * Number.EPSILON` creates enough tolerance for this instance.

```js
function equal(x, y, tolerance = Number.EPSILON) {
  return Math.abs(x - y) < tolerance
}

const x = 1000.1
const y = 1000.2
const z = 2000.3
console.log(equal(x + y, z, 2000 * Number.EPSILON)) // true
```

➡️ For more check [Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/EPSILON)
