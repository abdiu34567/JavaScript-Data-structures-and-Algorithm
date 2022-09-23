## Declaration with **let**: `Block Scope`

Any variables declared with `let` are in the closest block scope (meaning within the `{}` they were declared in)

```js
function scope3(print) {
  if (print) {
    let insideIf = '12'
  }
  console.log(insideIf)
}
scope3(true) // prints Error
```
