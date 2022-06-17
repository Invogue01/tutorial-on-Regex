# tutorial-on-Regex

What is Regex?<br>
Regex stands for Regular Expression and is a quick way to identify a pattern of characters. Regular expressions is not a programming language and instead used for pattern recognition, text mining, and input verification.

## Summary

Surprisingly, the idea did not come from the field of Computer science and actually related to the neuroscience.

In 1943 scientists named McCulloch and Pitts developed models that describe how the human nervous system works extended by Mathematician named Stephen Kleene in 1956 described these models using algebraic notation which became the backbone of regex and eventually in 1968, Ken Thompson was a mathematician and one of the leading UNIX developers implementing regular expressions in a text editor called ed.

That is the entry point of regex into the computing world.

In this tutorial I am going to use an example for email verifier regex and will explain each component of this expression.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. `

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

Anchors are these symbols which indicate the start and end of the regex script.
`^`indicates the start and `$`indicate the end of the regex script.

### Quantifiers

A regex quantifier `+` Match a certain quantity of the character or subexpression required immediately to its left.
For example, the regular expression `^([a-z0-9_\.-]+)@ ` tries to match one or more instances of `@` that begin with the `[a-z0-9_\.-]` and similarlity tries to match one of more instances of `.` after `([\da-z\.-]+)\.`
and `{2,6}` Matches the previous token [a-z\.] between 2 and 6 times, as many times as possible, giving back as needed.

### Grouping Constructs

Grouping constructs represent the subexpressions `(sub expressions)` of a regular expression and capture the substrings of an input string. <br>
in our example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. ` we can subcontruct the express into
<br>
User Name = `([a-z0-9_\.-]+)`
<br>
Email Provider= `([\da-z\.-]+)`
<br>
.com = `([a-z\.]{2,6})`

### Bracket Expressions

`[Bracket Expressions]` confirms the single or multiple characters range defind within the sqaure brakets and it is also case sensitive.
<br>
`[a-z0-9_\.-]` matching any alphabets between `a-z`case senstive and any numerics between `0-9` and symbols `.`,`_`,`-`
<br>
<br>
[\da-z\.-] Matching single digit character from `0-9 `and any character `a-z` case sensitive and symbols `.`,`-`
<br>
<br>
[a-z\.] Matching any character `a-z`(case senstive) and the character `.`

### Character Classes

`\d`Matches single character that is digit in our example Equivalent to [0-9].

### The OR Operator

`|` opreator is used to match the right and left character with in the string e.g `a | A`means the geretared expression can match lower | upper case character

### Flags

Flags are optional parameter which can be used to make the expression more dynamic for example `i` one of the tyoe of the flag can be used to match express search insentively.

### Character Escapes

character combination backslash `\` followed by a character represent a new line character in our example `[a-z0-9_\.-]`
character excape is used to Match a subexpression that is repeated in the input string.

## Author

<a href="https://github.com/zainuabidin">`Zain Ul Abidin`</a>

<a href="https://gist.github.com/zainuabidin/36fc0d5004f5126d92d02399ff3f953b#anchors">`link to Gist`</a>
