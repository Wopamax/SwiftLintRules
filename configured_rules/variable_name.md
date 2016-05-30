# rule_name
----------

# configuration_name : min_length
----------
- default: (warning: 3, error: 1)
- configured: (warning: 0, error: 0) // disabled

Although we mostly agree with this rule, the `minLength` property doesn't take into
account the context of the declaration. We often use short names such as `idx` when
iterating over an array, or `x`, `y` when manipulating frames. Of course, it doesn't
mean that we shouldn't pay specific attention to our variables names.

# Examples
----------
```
// indexes
if let idx = array.indexOf(someObject) { }
```

```
// frames & points
let x = CGPoint.zero.x
```

```
// mathematics often use single character variables
func polynomial(a: Float, b: Float, c: Float) -> Float
```
