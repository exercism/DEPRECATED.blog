+++
date = "2015-08-08"
title = "Updating an Exercise README"
+++

Instructions will, inevitably, be confusing. Not all the instructions, and not
all the time, but some certainly some instructions are confusing to some
people, some of the time.

Sometimes they're confusing because they're poorly worded. At other times,
they're outdated or downright wrong.

Or perhaps they just have a typo.

The Exercism exercise README treads a very fine line between useful ambiguity
and confusing vagueness. Because the README is the same whether you're solving
the problem in C++ or in Lua, the problem description needs to be high-level
enough to allow for the syntactic, semantic, and philosophical differences in
the various languages. In other words: no specific references to syntax or
datastructures.

Each language nails down the exact specification for the exercise in its own
test suite, which allows the language to treat the problem in a way that is
interesting and idiomatic.

## Contributing a Fix

If you want to fix an exercise README, then use the name of the directory that
the exercism was delivered in, e.g. `bob` or `hamming`, and find the
equivalent markdown file in the [shared metadata
repository](https://github.com/exercism/x-common), e.g. `bob.md` or
`hamming.md`.

[Fork the
repository](https://github.com/exercism/x-common/fork), commit your change,
and submit a pull request.

There aren't any rules about what a good exercism problem README looks like.
If in doubt, [open up a GitHub
issue](https://github.com/exercism/x-common/issues/new) describing your
suggestion.

If you get stuck on any of the steps or feel confused, overwhelmed or
intimidated, hit us up in the support chat. We're happy to do what we can to help
get your patch accepted!

