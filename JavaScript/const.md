## Declaration with **const** : `Block Scope`

Constants are block-scoped, much like variables declared using the `let` keyword.

The value of a constant can't be changed through `reassignment` and it can't be `redeclared`. However, if a constant is an `object` or `array` its properties or items can be `updated` or `removed`

```js
if (true) {
  const foo = 'foo'
  console.log(foo) // "foo"
}

console.log(foo) // Uncaught ReferenceError: foo is not defined
```
