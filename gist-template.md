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

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

This walkthrough was created by [Lindsay Lewis](https://github.com/lindslewis), a student full-stack web developer with the University of Washington. 

Lindsay is based out of Portland, Oregon. She is an Oregon State University English Literature alumni transitioning into the programming world.

You can find Lindsay spending her free time partaking in various fiber crafts, enjoying a quiet evening playing games, and tinkering away at her growing coding skills.
