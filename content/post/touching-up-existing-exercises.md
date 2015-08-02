+++
date = "2015-08-01"
title = "Touching Up Existing Exercises"
+++

_This post assumes that you'd like to make a change to a language-specific test
suite, or one of the language-specific supporting files (type definitions,
boilerplate code, etc)._

-------

Exercism exercises are not perfect. Shocking, I know.

Many of them are hastily conceived, and implemented without too
much thought. This isn't done out of carelessness, but from a sense
of experimentation.

Also, exercises are often made up for one language, and then later used
to bootstrap a other languages. Things that are idiomatic in one language,
are often awkward in others.

To make matters more interesting, language tracks are often started by a
programmer who typically doesn't work in that language. It's a fun and
challenging way to dig into a new language.

This means that we often make choices that are informed by experiences gained
from working in other languages. As the saying goes, you can write FORTRAN in
any language.

Oh, yeah: also we're human, not humanoids. We have extremely limited
cognitive resources, which leads us to have charming idiosyncracies and
make interesting mistakes.

## Exercises Evolve

Over time, the exercises improve.

Someone notices that a test suite is missing an important edge case or that
the README is confusing, or an assertion is wrong. Or there's a typo. Or
there's a simpler, more expressive way to write a test. And once in a
while--crucially, for exercism--someone decides to fix it.

_(Thank you for that!)_

Some changes to the test suites will invalidate existing solutions that people
have submitted.

We think this is totally fine.

We would much rather launch early and iterate than try to get the exercises
right the first time around. It's only when we get a bunch of people having
conversations about the solutions that we really discover what makes a problem
interesting, and in what way it can be improved. Sometimes the best edge
cases are discovered because someone submits a solution that passes the tests,
but that make interesting or unusual assumptions.

Occasionally changing the exercises themselves causes people to leave feedback
saying that a solution doesn't pass the tests. This is technically true, but
since the solution passed the tests at the time it was written, it's generally
more useful to just discuss the code as it is, rather than enforce strict
adherence to the most recent version of the tests.

Some language tracks have implemented a simple, manual versioning system to
help avoid unnecessary discussions about failing the current test suites.

## Making Your First Contribution

It can be confusing and intimidating to figure out how to fix even a tiny
thing in a small project, much less a sprawling 50 repository beast like
Exercism.

The process boils down to this:

1. Setting up a development environment.
1. Making the change.
1. Submitting a patch.

### Setting up a Development Environment

The trickiest part is usually figuring out which repository the change needs
to happen in. Exercism has over 20 different active language tracks, and
more are being added all the time.

We've separated each language track into its own repository. This makes it
possible to work on a track without worrying about the overall exercism
eco-system and particularly without having to install irrelevant languages and
tools.

Also, it lets us give different people access to different language
tracks so that they can review patches and discuss language-specific issues
without causing a bunch of irrelevant noise for maintainers of other tracks.

Each language on Exercism might be referred to by full name (e.g. Common Lisp
or C++), or by a url-friendly "slug" (e.g. lisp or cpp). The track
repositories are named using the url-friendly slug:

    http://github.com/exercism/x{SLUG}

The slug is used in many places, among them the path that the CLI uses when
downloading exercises to your local machine:

    /home/you/exercism/{SLUG}

So if you'd like to make a change to a haskell exercise, you'd [fork the
repository](https://help.github.com/articles/fork-a-repo/) at
[github.com/exercism/xhaskell](https://github.com/exercism/xhaskell), and to
tweak something in F# you would go to
[github.com/exercism/xfsharp](https://github.com/exercism/xfsharp).

Check out the README in the track repository to see if there are any special
dependencies for contributing to that language. Often all you need is a
running language environment along with the relevant testing library.

### Making the Change

An exercism exercise consists of a **README**, a **test suite**, and a
**reference solution**.

The README is shared between all the language tracks, and lives in a [separate
repository](https://github.com/exercism/x-common), and the process will be
[slightly
different](https://github.com/exercism/x-api/blob/master/CONTRIBUTING.md#metadata).

The reference solution does not need to be great code; it's currently not used for
anything beyond making sure that the test suite is coherent. It will be named
something with `example` or `Example` in the path. In most languages this will be part
of the file name, but it might also be a subdirectory.

_Please be sure to update the reference solution so that it passes the updated
test suite._

Some language tracks are experimenting with generating test suites from [shared
test data](https://github.com/exercism/todo/issues/13). If this is the case,
then you will need to update either the generator or the test data, and then
regenerate the exercise.

If the exercise is versioned, then the test suite will probably have a
_book-keeping_ type test at the very bottom that asserts against a value in
the reference solution. If the change you're making is backwards-incompatible,
then please increment the version in both the test suite and the reference
solution.

### Submitting a Patch

You don't need to get it perfect the first time around; we'll work with you to
get the patch merged. If you're not familiar with git, we can help you out
with that as well.

When making your commit, please take the time to compose a descriptive commit
message. One of the best guidelines to [writing good commit
messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
comes from Tim Pope.

If you're making a change to a specific exercise, please put the name of the
exercise in the subject line of the commit. E.g.

    hamming: Add test case for strands of unequal length

If you have multiple unrelated changes, please make separate pull requests for
each one.

Once you've submitted a pull request, one or more of the track maintainers
will review it. Some tracks are less active and might not have someone
checking in every day. If you don't get a response within a couple of days,
feel free to ping us in the [support
chat](https://gitter.im/exercism/support).

Most tracks are running some form of continuous integration on Travis CI.
You can check out the `.travis.yml` file to see what is being tested, and how.
If the build fails and you're not sure why, don't hesitate to ask us about it,
we'll help you figure it out and fix it.

## Thank you!

We are grateful for any help in making Exercism better.

Feel free to jump in the [support chat](https://gitter.im/exercism/support) or
open a GitHub issue in the language-specific repository if you're unsure about
the change you want to make. We'll do everything we can to help you get started.

