## **Maximums**

`Number.MAX_SAFE_INTEGER` returns the `largest integer`

```js
Number.MAX_SAFE_INTEGER + 1 === Number.MAX_SAFE_INTEGER + 2 // true
```

This returns true because it cannot go any `higher`. However, it does not work for floating-point decimals

```js
Number.MAX_SAFE_INTEGER + 1.111 === Number.MAX_SAFE_INTEGER + 2.022
// false
```

`Number.MAX_VALUE` returns the `largest floating-point` number possible.
`Number.MAX_VALUE` is equal to `1.7976931348623157e+308`

```js
Number.MAX_VALUE + 1 === Number.MAX_VALUE + 2 // true
```

Unlike like `Number.MAX_SAFE_INTEGER`, this uses `double-precision floating-point` representation and works for floating points as well

```js
Number.MAX_VALUE + 1.111 === Number.MAX_VALUE + 2.022 // true
```
