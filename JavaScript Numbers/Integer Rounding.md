## **Integer Rounding**

Since JavaScript uses `floating point` to represent all numbers, integer division does not work

Integer division is division in which the fractional part (`remainder`) is discarded

> In JavaScript to implement `integer division`
>
> - Math.floor - rounds `down` to nearest integer
> - Math.round - rounds to `nearest` integer
> - Math.ceil - rounds `up` to nearest integer

```js
Math.floor(0.9) // 0
Math.floor(1.1) // 1
Math.round(0.49) // 0
Math.round(0.5) // 1
Math.round(2.9) // 3
Math.ceil(0.1) // 1
Math.ceil(0.9) // 1
Math.ceil(21.01) // 22
```
