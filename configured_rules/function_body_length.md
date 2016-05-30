# function_body_length
----------

# max_length
----------
- default: 40
- configured: 60

We feel like if written correctly, 40 lines shouldn't be too hard to read. We don't
beleive that separating functions just to keep its number of lines under 40 might be
worth it. Although, after 60 lines it might be a little trickier. This value might
change after using swiftlint for a while though.  
Some methods (`loadView` for example) might be well above 60 lines and won't be
complicated to read too. You can punctually disable this rule if needed, as long
as the code remains simple to read.
To do so, simply use this line above the function : `// swiftlint:disable:next function_body_length`.


# Examples
----------
_N/A_
