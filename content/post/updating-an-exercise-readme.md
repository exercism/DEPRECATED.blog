+++
date = "2015-08-08"
title = "Updating an Exercise README"
+++

## Challenge

The Exercism exercise README treads a very fine line between useful ambiguity and confusing vagueness. Because the README is the same whether you're solving the problem in C++ or in Lua, the problem description needs to be high-level enough to allow for the syntactic, semantic, and philosophical differences in the various languages. In other words: no specific references to syntax or data structures of a specific language can be used to further clarify a problem.

However, within this purposeful ambiguity might lie some opportunities for making an exercise description more clear. Typical issues to be attentive to:

- poorly worded sentences
- outdated information
- incorrect directives
- typos

Each language's test suite provides the precise specification for the exercise, which allows the user to view the problem from a perspective that is interesting and idiomatic for that specific language.

## Contributing with a README Fix

If you want to fix an exercise README, then use the name of the directory that the exercism was delivered in, e.g. `bob` or `hamming`, and find the equivalent markdown file in the [shared metadata repository](https://github.com/exercism/x-common), e.g. `bob.md` or `hamming.md`.

[Fork the repository](https://github.com/exercism/x-common/fork), commit your change, and submit a pull request.

There aren't any rules about what a good exercism problem README looks like. If in doubt, [open up a GitHub issue](https://github.com/exercism/x-common/issues/new) describing your suggestion.

If you get stuck on any of the steps or feel confused, overwhelmed or
intimidated, hit us up in the [support chat](https://gitter.im/exercism/support). We're happy to do what we can to help get your patch accepted!
