### force_try

I'm not sure about this one. `try`/`catch` blocks are super bothersome as we rarely have to handle the exception. But the force `try` can be replaced with a conditional `try`, that doesn't trigger a warning.
```swift
func a() throws {}; ↓ _ = try? a()
```

### force_unwrapping

This is the same as the `force_cast` rule. Plus, keeping this rule comes in direct contradiction `cyclomatic_complexity` rule, as it forces us to `if let` every variable.
