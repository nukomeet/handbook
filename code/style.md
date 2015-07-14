# Style

Common style over all codebase is essential for shared codebase. Otherwise most time there will be holy war between coworkers about bad and good practices. This is reason why this section exists, to create common, shared practices. If some of them doesn't suit you then you can create pull request where we can discuss if it is better than currently used one. If it isn't accepted then please, keep in line.

## Line endings

As most of us works on Mac OS X and GNU/Linux then all codebase should use Unix line endings (single `0x0A` line feed character, commonly escaped as `\n`).

### New line at the end of file

This is tradition from first versions of Unix that all text files has empty line at the end to make it easier to count lines in file (i.e. `wc -l` just needed to count occurrences of `\n` without checking border cases).

Enable this feature in various editors:

- Vim and NeoVim has this enabled by default
- Sublime Text 3: ensure that `ensure_newline_at_eof_on_save` is set to `true`
- Atom: check [@kevinsawicki comment](https://github.com/atom/atom/issues/4741#issuecomment-67892695)
- IntelliJ: [Ensure line feed at file end on save](http://stackoverflow.com/a/16761228/1017941)


## Spaces over tabs

In general spaces give you more control. This is why [experienced programmers prefer spaces](http://stackoverflow.com/research/developer-survey-2015#tech-tabsspaces).

How many spaces? In most languages you should use 2, except where it is prohibited, or given styleguide states otherwise.

### Exceptions

In some cases you cannot use spaces, as syntax depends on them. The most popular one (and only one in this guide) is `Makefile`. Keep in mind that you should use only tabs there.

## Code smells

We all should work on code that is easy to read and fun to maintain. To keep it that way you should learn and keep to some simple rules:

### Do not Repeat Yourself

If some code has similar purpose and is needed in more than 2 places then it should be a method (or macro). Always. Period.

### Keep thing simple

If you _think_ that client would like to have some feature that (s)he doesn't specified then, belive me, they dont need it at all. Don't overcomplicate codebase just in sake of imaginary features. Keep things as simple as possible, but keep in mind that this must be replaceable.