# Gist Regex Stong Passowrd

Regex or Regular expressions are patterns used to match character combinations in strings. In this tutorial we'll break down a Regex for a stong password.

## Summary

We'll be looking at how the following Regex is used to match a strong password:

```js
var passwordRegex = /(?=^.{6,}$)((?=.*\w)(?=.*[A-Z])(?=.*[a-z])(?=.*[0-9])(?=.*[|!"$%&\/\(\)\?\^\'\\\+\-\*]))^.*/g;
```

## Table of Contents

- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Anchors](#anchors)
- [Lookaround](#lookaround)
- [Author](#author)

## Regex Components

```js
var passwordRegex = /(?=^.{6,}$)((?=.*\w)(?=.*[A-Z])(?=.*[a-z])(?=.*[0-9])(?=.*[|!"$%&\/\(\)\?\^\'\\\+\-\*]))^.*/g;
```

## Quantifiers 
## `* {}`

Quantifiers indicate that the preceding token must be matched a certain number of times. By default, quantifiers are greedy, and will match as many characters as possible.

`*` (Star): Matches 0 or more of the preceding token.
e.g.
`.*\w` Matches any word or charcter.

`{}` (Quantifier): Sets either an exact amount, min and max, or more than one copies of the sequence before the quantifiers.
e.g.
`{6,}` Matches 6 or more of the preceding token.

## Character Classes 
## `[] . \w`

Character classes match a character from a specific set. There are a number of predefined character classes and you can also define your own sets.

`[*-*]` (Range): Matches a character having a character code between the two specified characters inclusive.
e.g.
`[A-Z]` Matches any character between A and Z.

`[***]` (Character Set): Match any character in the set.
e.g.
`[|!"$%&\/\(\)\?\^\'\\\+\-\*]`

`.` (Dot): Matches any character except linebreaks. Equivalent to [^\n\r].

`\w` (Word): Matches any word character (alphanumeric & underscore).Equivalent to [A-Za-z0-9_].

e.g. `.*\w` Matches any word or charcter.

## Flags 
## `g`

Expression flags change how the expression is interpreted. Flags follow the closing forward slash of the expression (ex. /.+/igm ).

`g` (Global Search): Retain the index of the last match, allowing subsequent searches to start from the end of the previous match. Without the global flag, subsequent searches will return the same match.

## Grouping and Capturing 
## `()`

`()` (Capturing Group): Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.
e.g.
`((?=.*\w)(?=.*[A-Z])(?=.*[a-z])(?=.*[0-9])(?=.*[|!"$%&\/\(\)\?\^\'\\\+\-\*]))`

## Anchors 
## `^ $`

`^` (Beginning): Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. This matches a position, not a character.

`$` (End): Matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.

e.g.
`^.{6,}$`

## Lookaround
## `(?*)`

`(?=)` (Positive Lookahead): Matches a group after the main expression without including it in the result.
e.g.
`(?=^.{6,}$)`

### Author

[gg](https://github.com/ggruiz7) - A work in progress.
