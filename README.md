# Matching a Hex Value With Regex

A regex or regular expression is a search pattern which is a line of specific characters that allows you to define dynamic parameters in JavaScript.

## Summary

The following tutorial will show you how to match a hex value in JavaScript using this regular expression `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

You see that this regex starts and ends with a `/` which signifies that the expression is literal.

### Anchors

After the first `/` you'll see the next character in the expression is a `^`, this signifies an anchor. The `^` achor means that the string will start with the exact characher that follows it. So we can see that our hex value string will start with a `#` -- as all hex values do.

At the end of our regex, you'll see the exprssion ends with a `$` which is also an achor. This indicates that the expression will end with whatever parameter preceeds it. So our hex value will end with either a character between "a" and "f", or with a number between 0 - 9. The string can be all letters.

### Quantifiers

Our quantifiers are found in the curly brackets. We see 2 quantifiers -- `{6}` and `{3}`. This means the first part of our string must be exactly 6 characters long, and the second part of our string must be exactly 3 characers long. The 2 "parts" of our expression are separated by an "OR Operator" which is the pipe `|`.

### Grouping Constructs

There are no Grouping Constructs used in this regex, but they fall into 2 categories -- Capturing and Noncapturing. They can be used for several different reasons, most prominently they are used to match a subexpression within an input string.

### Bracket Expressions

In our regex, we see 2 sets of bracket expressions -- which is anything inside the square brackets `[]`. In the expressions both sets of bracket expressions look like this `[a-f0-9]`. This parameter is allowing any lower case letter between "a" and "f", and/or any number between 0 - 9. (`#000000`, `#abcdef`, `#123abc` are all examples of accepted strings).

### Character Classes

The only characeter classes we find in this regex are the [Bracket Expressions](#bracket-expressions), which we go over in the previous section.

### The OR Operator

We will find one "OR Operator" in this regex which is the pipe in the middle of the expression (`|`). This tells us that our hex value can either match a typical 6 character hex value, or it can be a shorthand 3 character hex value. Either option would be accepted. For example: `#000000` or `#000` (both are the hex value for black) would satisfy the regex parameters.

### Flags

A flag in a regex is an extra letter that comes after the last back slash of the expression. Flags define addional functionality in an expression, such as global search, case insensitive search and multi line search.

You'll see that we do not have any flags in this expression.

### Character Escapes

A Character Escape is when a backslash is used inside of a regex to escape a special character that can be used inside a string. For example, you might see a backslash in front of a curly bracket (`/{`), which means that the curly bracket can be used inside of the string. This is common with special character parameters.

There are no Character Escapes in this particular expression.

# Author

This regex tutorial was written by Gwen Ewasko. You can find her online [here](https://github.com/gwenewasko).
