## **JavaScript Numbers**

Number operators in JavaScript

- addition `(+)`
- subtraction `(-)`
- division `(/)`
- multiplication `(*)`
- modulus `(%)`

### Number System

JavaScript uses a `32-bit floating-point` representation for numbers

```js
0.1 + 0.2 == 0.3 //false
0.1 + 0.2 === 0.3 //false
```

To understand why 0.1 cannot be represented properly as a 32-bit floatingpoint number, you must understand `binary`. Representing many decimals in binary requires an `infinite number` of digits. This because binary numbers are represented by **2<sup>n</sup>**
where `n` is an integer.

While trying to calculate 0.1, long division will go on `forever`
