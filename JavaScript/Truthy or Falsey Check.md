## **Truthy/Falsey Check**

True/false checking is used in `if` statements. In many languages, the parameter inside the `if()` function must be a `boolean` type. However, JavaScript (and other dynamically typed languages) is more flexible with this. Here’s an example:

```js
if(node){
...
}
```

Here, `node` is some variable. If that variable is `empty`, `null`, or `undefined`, it will be
evaluated as `false`

Here are commonly used expressions that evaluate to

`false:`

- false
- 0
- Empty strings ('' and "")
- NaN
- undefined
- null

` true:`

- Any number other than 0
- Non-empty strings
- Non-empty object

```js
var printIfTrue = ''
if (printIfTrue) {
  console.log('truthy')
} else {
  console.log('falsey') // prints 'falsey'
}
```

### **===** vs **==**

JavaScript is a `scripting language`, and variables are not assigned a type during `declaration`. Instead, types are `interpreted` as the code runs.

`===` is used to check `equality` more strictly than `==`

`===` checks for both the
`type` and the `value`, while `==` checks only for the `value`.

```js
1 "5" == 5 // returns true
2 "5" === 5 // returns false
```

"5" == 5 returns true because "5" is coerced to a number before the comparison.

On the other hand, `"5" === 5` returns `false` because the type of `"5"` is a `string`, while 5 is
a `number`

### Objects

```js
var o1 = {}
var o2 = {}

o1 == o2 // returns false
o1 === o2 // returns false
```

Although these objects are equivalent (`same properties` and `values`), they are not
equal. Namely, the variables have different `addresses` in memory. This is why most JavaScript applications use utility libraries such as lodash or underscore, which have the `isEqual(object1, object2)` function to check two objects
or values strictly. This occurs via implementation of some property-based equality
checking where each property of the object is compared.

In this example, each property is compared to achieve an accurate object equality result

```js
function isEquivalent(a, b) {
  // arrays of property names
  var aProps = Object.getOwnPropertyNames(a)
  var bProps = Object.getOwnPropertyNames(b)

  // If their property lengths are different, they're different objects
  if (aProps.length != bProps.length) {
    return false
  }

  for (var i = 0; i < aProps.length; i++) {
    var propName = aProps[i]

    // If the values of the property are different, not equal
    if (a[propName] !== b[propName]) {
      return false
    }
  }

  // If everything matched, correct
  return true
}
isEquivalent({ hi: 12 }, { hi: 12 }) // returns true
```

However, this would still work for objects that have `only` a `string` or a `number` as the
property.

```js
var obj1 = { prop1: 'test', prop2: function () {} }
var obj2 = { prop1: 'test', prop2: function () {} }

isEquivalent(obj1, obj2) // returns false
```

This is because `functions` and `arrays` cannot simply use the `==` operator to check for
equality.

```js
var function1 = function () {
  console.log(2)
}
var function2 = function () {
  console.log(2)
}
console.log(function1 == function2) // prints 'false'
```

Although the two functions perform the same operation, the functions have different `addresses` in memory, and therefore the equality operator returns `false`.

The primitive equality check operators, `==` and `===`, can be used `only` for `strings` and
`numbers`.

To implement an `equivalence` check for `objects`, each property in the object needs to be `checked`
