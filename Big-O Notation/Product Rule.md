## Product Rule : `Multiply Big-Os`

> `If f(n) is O(h(n)) and g(n) is O(p(n)), then f(n)g(n) is O(h(n)p(n))`

```JavaScript
function (n){
  var count =0;
  for (var i=0;i<n;i++){
    count+=1;
    for (var i=0; i<5*n;i++){
        count+=1;//line 6
    }
  }
  return count
}
```

In this example, `f(n) = 5n*n` because line 6 runs 5n times for a total of n iterations.
Therefore, this results in a total of <code>5n<sup>2</sup></code>
operations. Applying the coefficient rule, the result is that <code>O(n)=n<sup>2</sup></code>
