## Random Number Generator

JavaScript has a `built-in`
function for generating numbers

> `Math.random()`

Math.random() returns a float between `0` and `1`

- Math.random() \* 100; // floats between 0 and 100
- Math.random() \* 25 + 5; // floats between 5 and 30
- Math.random() \* 10 - 100; // floats between -100 and -90

To get random integers

- Math.floor(Math.random() \* 100); // integer between 0 and 99
- Math.round(Math.random() \* 25) + 5; // integer between 5 and 30
- Math.ceil(Math.random() \* 10) - 100; // integer between -100 and -90
