# Regex Email - Matching an E-mail

Regex, or Regular Expression is a sequence of characters that specifies a specific pattern in text. It is mostly used in search engines or in this case, validating a certain pattern of text. They are practically universal with any programming languages

## Summary

This readme is made to carefully explain the Regex pattern that allows you to identify and validate an e-mail. i.e: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

It is easier to understand each regex component if they are separated into parts, Below here will explain in detail.

### Anchors

There are two anchor tags used `^` which denotes the beginning of a string or line and `$` which which denotes the end. since the mutiline flag `(m)` is not enabled it only denotes a string for both, not a line 

### Quantifiers

The quantifiers used in this regex are the `+` operator that lets use match 1 or more of the preceding token. This allows us to validate the email name, the email provider name, and the domain extensions of the email. The other quantifier `{2,6}` indicates a range between 2 and 6 of the token which are the domain names. Most popular domain names are normally 4 characters, but they are a few exceptions.

### Grouping Constructs

As said before, but now in greater detail, there are a total of three grouping constructs. The first construct `([a-z0-9_\.-]+)` validates the email name, the second construct `([\da-z\.-]+)` validates the email provider name, and the third construct `([a-z\.]{2,6})` which validates the domain name.

### Bracket Expressions

Anything in the bracket expressions `[]` are a range of characters that we want to match. The first bracket expression. 

`[a-z0-9_\.-]` indicates characters in the range of "a" and "z", characters in the range of "0" and "9" and the three characters "_", "-" and ".".
`\da-z\.-]` indicates any digit characters, characters in the range of "a" and "z", and the two characters "." and "-".
`[a-z\.]` indicates characters in the range of "a" and "z", and the character ".".

### Character Classes

Other than the character ranges `[a-z]` and `[0-9]` which indicated the range between these characters the `\d` class indicates a digit character similar to `[0-9]`.

### The OR Operator

The OR operation `|` is not used in this expression nor it couldn't be used in place of established character classes.

### Flags

Flags are regex characters that are placed at the end of a regex after the second slash `/`. They define additional functionality like the `i` flag that ignores case sensitivity. Currently there's no flag used for this specific expression

### Character Escapes

The backslash of a character excape `\` helps indicate that the regex should look for a specific character instead of a begining or end of a special expression: bracket, classes, ect. In this case the `\.` character escape is used to 

## Author

This has been a project by Mikhail Sookwah, you can find more at https://github.com/Mikhail25