## **Minimums**

`Number.MIN_SAFE_INTEGER` returns the `smallest integer`

Number.MIN_SAFE_INTEGER is equal to `-9007199254740991`

```js
Number.MIN_SAFE_INTEGER - 1 === Number.MIN_SAFE_INTEGER - 2 // true
```

This returns `true` because it cannot get any `smaller`. However, it does not work for
floating-point decimals

```js
Number.MIN_SAFE_INTEGER - 1.111 === Number.MIN_SAFE_INTEGER - 2.022 // false
```

`Number.MIN_VALUE` returns the `smallest floating-point` number possible.

Number.MIN_VALUE is equal to `5e-324`. This is not a negative number since it is the
smallest floating-point number possible and means that Number.MIN_VALUE is actually
`bigger` than Number.MIN_SAFE_INTEGER

Number.MIN_VALUE is also the closest floating point to `zero`

```JavaScript
Number.MIN_VALUE - 1 == -1; // true
```
