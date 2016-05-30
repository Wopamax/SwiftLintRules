# SwiftLint configuration discussion

## Rejected rules proposal

### cyclomatic_complexity

I feel this may lead to spaghetti code, as the easy response to this rule would be to multiply useless methods only called once in the block causing the warning. This makes the code hard to read and maintain.


### force_try

I'm not sure about this one. try/catch block are super bothersome as we rarely have to handle the exception. But the force try can be replaced with a conditional try, that doesn't trigger a warning.
```swift
func a() throws {}; ↓ _ = try? a()
```


### force_unwrapping

This is the same as the `force_cast` rule. Plus, keeping this rule comes in direct contradiction `cyclomatic_complexity` rule, as it forces us to `if let` every variable.


### function_body_length

I'm not too sure about this. I feel that the 40 lines limit is a bit low, in particular with `loadView` overrides that often are longer (and that's not an issue for me).


### line_length

Just how are we supposed to respect this rule? Swift is so verbose...


### variable_name

Although I mostly agree with this rule, it has a `minLength = 3` that I don't like. One character variables are very frequent, and used with reason.
```swift
let x = CGPoint.zero.x // x, y and z... that would be stupid to rename those
func polynomial(a: Float, b: Float, c: Float) -> Float // mathematics often use single character variables
```
