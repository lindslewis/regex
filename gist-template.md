# Regex: Matching Hex Values 

Regular expressions, or regexes, allow users to have a less restrictive search field, opening up their searches to broader and more dynamic search variables. A regex is made up of a string of characters to define a pattern for said search.

The characters used in a regex include letters, digits, and special characters.

## Summary

The regex that we will be looking over today is for "Matching Hex Values." 

This string of characters for the search pattern is as follows:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

I will be reviewing this regex's anchors, quantifiers, grouping constructs, bracket expressions, character classes, flags, escapes and the OR operator and how each of these pertains to matching matching hex code values.


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

### Anchors

The anchors, `^` and `$`, are both used in the Matching Hex Values regex pattern.

The carrot, `^`, indicates the beginning of a line or string. This indication shows that the following character must show at the beginning of the string.

The `$` anchor is used to designate the end of a string. 

For example,

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

The pound sign following the carrot (`^#`), indicates that the beginning of all hex codes that are attempting to be matched must beginning with a pound sign.

`#ff748c`

`#000bad`

The two above hex codes illustrate this, that they both utilize a pound sign right before their character string that defines their color. 

Regarding the end of string anchor, `$`, the hex code requires the end of the string to be everything contained within the parantheses.

### Quantifiers

Regex quantifiers include:
`+`, `?`, `*`, and `{X, Y}`.

Our example code for matching hex values contains several quantifiers. 

In our matching hex values regex code snippet, there are two iterations of the last quantifier, the `{x, y}`. This quantifier refers to x being the least amount of times a character repeats, while y refers to the most amount of times said character may repeat. 

In the code, we see the quantifiers `{6}` and `{3}`. Quantifiers refer to the objects living to their left, so the six is in direct reference to the object living within the brackets, `[a-f0-9]` and the three is in direct reference to it's own bracketed object of the same value. Since there is no y value found in these instances, that means that the first one will repeat *exactly* six times, and the second will repeat *exactly* three times. Those repetitions may all be the same character, or, since their referenced code is a [bracket expression](#bracket-expressions), which we will discuss shortly, it may be any characters within that bracket expressions iterated range.

### Grouping Constructs

Grouping constructs in regex expressions refer to the capture of characters within a pair of parantheses. 

If a pattern lives within a pair of parantheses in a regex expression, then that pattern will be captured as a group, meaning all of those characters within that group will be used in the sorting of the data within the search parameters. 

In the case of our hex value patterns, we have one set of parantheses, and can be seen below:

`([a-f0-9]{6}|[a-f0-9]{3})`

Since the paranthesis makes up the majority of the regex pattern. This particular pattern utilizes an [OR expression](#the-or-operator), which we will cover soon, however that means there will be some variability in what is able to be matched by the grouped characters.

### Bracket Expressions

As seen in our grouping constructs, there are two sets of bracket expressions found in our hex value pattern. 

Both of these bracket expressions contain the same range, `[a-f0-9]`.

The above bracket expression means that the grouping may contain any lower case letters that range from a through f, and may contain any integers that range from 0 to 9. Since these bracket expressions are also paired with quantifiers (the first paired with a quantifier of 6, and the second paired with a quantifier of 3), it means that any character within the parameters set by the bracket expression may repeat 6 times and 3 times. 

For example, here is our regex pattern:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Now, if we pair the required pound sign with the first set of brackets and it's quantifier, we could end up with a pattern looking like:

`#af0934`

or

`#6aa84f`

The above two hex codes turn out two colors, the first being a darker magenta, and the second being a lighter forest green. If we look through the pattern exhibited in both of these, they fit the requirements laid out by the anchor (the necessary beginning of the code with a `#`), the brackets (the string of characters following the anchor element can be any lower case letter `a` through `f`, and any integer `0` to `9`), and the quantifier (6 characters that follow the parameters that the bracket expressions set).

The same holds true for the second set of brackets, some examples of such a pattern would be:

`#fc9`

or

`#b58`

The above two hex codes also still hold true for the set parameters of lower case letters ranging from `a` to `f` and integers ranging from `0` to `9`. Since it is the second set of brackets, they have the quantifier of 3, so there are only three characters instead of the six from before. 

In the cases where there are only 3 characters following the beginning anchor, these hex codes are shorthand versions of their longer companions. Specifically, the 3 character hex code is used when the red, green, and blue components are all the same (typically seen as rr, gg, and bb).

The above hex codes represent a light salmon pink and lavender. If written in long hand form, they would appear as such:

`#fc9` would be the same as `#ffcc99`
`#b58` would be the same as `#bb5588`


### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

This walkthrough was created by [Lindsay Lewis](https://github.com/lindslewis), a student full-stack web developer with the University of Washington. 

Lindsay is based out of Portland, Oregon. She is an Oregon State University English Literature alumni transitioning into the programming world.

You can find Lindsay spending her free time partaking in various fiber crafts, enjoying a quiet evening playing games, and tinkering away at her growing coding skills.
