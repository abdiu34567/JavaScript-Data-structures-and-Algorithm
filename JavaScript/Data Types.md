## JavaScript data types

The set of types in the JavaScript language consists of `primitive values` and `objects`

**Primitive values :**

- _Boolean type_
- _Undefined type_
- _Number type_
- _Function type_
- _String type_
- _Symbol type_

> `Determining types using the typeof operator`

```js
var is20 = false // boolean
typeof is20 // boolean

var age = 19
typeof age // number

var lastName = 'Bae'
typeof lastName // string

var fruits = ['Apple', 'Banana', 'Kiwi']
typeof fruits // object

var me = { firstName: 'Sammie', lastName: 'Bae' }
typeof me // object

var nullVar = null
typeof nullVar // object

var function1 = function () {
  console.log(1)
}
typeof function1 // function

var blank
typeof blank // undefined
```
