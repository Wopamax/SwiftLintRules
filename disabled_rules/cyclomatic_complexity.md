# rule_name
----------

# Why was this rule disabled :
----------
Even though the cyclomatic complexity sometimes helps calculate how hard a method
is to maintain, it isn't really always applicable to human-readability. For example,
a simple method with a `switch` case over an `enum` value can have a very high
cyclomatic complexity, but would be simple to read for a programmer.

# Examples
----------
```
// cyclomatic_complexity is 6, which means "hard to read"
switch deepLinkingPath {
  case "home":      presentHome()
  case "product":   presentProduct()
  case "lists":     presentLists()
  case "favorites": presentFavorites()
  case "settings":  presentSettings()
}
