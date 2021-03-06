# SwiftLint
----------
As a reminder, [SwiftLint](https://github.com/realm/SwiftLint) is a _linter_, it
enforces a list of rules that should be followed by the developer when coding.  
This enforces a team to follow the same rules, and usually helps maintaining a
healthy codebase.  

Don't forget to update SwiftLint regularely to get the most recent rules.

# Introduction
----------
This repository holds the default `.swiftlint.yml` configuration file
that should be used for new projets at Wopata.  

Each time SwiftLint is updated, we should analyze the rules that have been added, and configure them in the `.swiftlint.yml` file.  

Disabled or configured rules should have a `rule_name.md` file in the `{configured,disabled}_rules` folder. You should copy the `template/{configured,disabled}.md` file and start from here to explain the rationale.  

By default, we should optin for all opt_in_rules (you can see them by running `swiftlint rules`), and disable if needed.

# Setup
----------
You should follow the instructions on SwiftLint's repository to add the linter
in the build phase, so there's issues will be highlighted whithin Xcode directly.

To get the right `.swiftlint.yml` file in your repository, you can simply add this
repository as a submodule :
```sh
git submodule add git@github.com:Wopamax/SwiftLintRules.git
ln -s SwiftLintRules/.swiftlint.yml
```
Yay, you're done.


# Disabled rules
----------
 - [force_cast](disabled_rules/force_cast.md)
 - [line_length](disabled_rules/line_length.md)
 - [cyclomatic_complexity](disabled_rules/cyclomatic_complexity.md)

# Configured rules
----------
 - [variable_name](configured_rules/variable_name.md)
 - [function_body_length](configured_rules/function_body_length.md)
