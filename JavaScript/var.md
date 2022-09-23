## Declaration with **var** : `Functional Scope`

In JavaScript, var is one keyword used to declare variables. These variable declarations
“float” all the way to the top. This is known as `variable hoisting`

Variables declared at the
bottom of the script will not be the last thing executed in a JavaScript program during
runtime

```js
function scope1() {
  var top = 'top'
  bottom = 'bottom'
  console.log(bottom)
  var bottom
}
scope1() // prints "bottom" - no error
```

The `bottom` variable declaration, which was at the last line in the function, is floated to the `top`, and logging the variable works

```js
function scope1() {
  var top = 'top'
  var bottom
  bottom = 'bottom'
  console.log(bottom)
}
scope1() // prints "bottom" - no error
```

The key thing to note about the `var` keyword is that the scope of the variable is the
`closest function scope`

```js
function scope2(print) {
  if (print) {
    var insideIf = '12'
  }
  console.log(insideIf)
}
scope2(true) // prints '12' - no error
```

⬆️ in this block of code, the scope2 function is the function scope closest to the `print`
variable

This function is equivalent to the following ⬇️

```js
function scope2(print) {
  var insideIf
  if (print) {
    insideIf = '12'
  }
  console.log(insideIf)
}
scope2(true) // prints '12' - no error
```

```js
var a = 1
function four() {
  if (true) {
    var a = 4
  }

  console.log(a) // prints '4'
}
```

4 was printed, not the global value of 1, because it was redeclared and available in
that scope
