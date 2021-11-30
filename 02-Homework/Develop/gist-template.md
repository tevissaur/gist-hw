# Regex Tutorial: Matching an email address

Ever wondered how the following jumble of characters:
    `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
is able to find an email inside of a string? 
Here in this tutorial, I will breakdown this regular expression and explain how each regex function operates. 
## What is a regular expression?

It is a sequence of characters that defines a specific pattern. When included in code, regular expressions are used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also handy in trying to validate input.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

# Regex Components

## Anchors
### Example: <span style="color:red">/^</span>`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`<span style="color:red">$/</span>
Matches the beginning and the end of the string, or the beginning and end of a line if the multiline flag (m) is enabled. This matches a position, not a character.

## Quantifiers
### Example: `/^([a-z0-9_\.-]`<span style="color:red;">+</span>`)@([\da-z\.-]`<span style="color:red;">+</span>`)\.([a-z\.]`<span style="color:red;">{2,3}</span>`)$/`
- Plus ( `+` )
    - Matches 1 or more of the preceding token.
- Star ( `*` )
    - Matches 0 or more of the preceding token
- Quantifiers ( `{2,3}` )
    - Matches the specified quantity of the previous token. {2,3} will match 2 to 3. {3} will match exactly 3. {3,} will match 3 or more.
## Grouping Constructs
### Example: `/^`<span style="color: red;">([a-z0-9_\.-]+)</span>`@`<span style="color: red;">([\da-z\.-]+)</span>`\.`<span style="color: red;">([a-z\.]{2,6})</span>`$/`
`()`
- Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.
## Bracket Expressions
### Example: `/^(`<span style="color: red;">[a-z0-9_\.-]</span>`+)@(`<span style="color: red;">[\da-z\.-]</span>`+)\.(`<span style="color: red;">[a-z\.]</span>`{2,6})$/`
Bracket expressions are a special kind of character class. Bracket expressions match one character out of a set of characters, just like regular character classes. They use the same syntax with square brackets. A hyphen creates a range, and a caret at the start negates the bracket expression.
## Character Classes
### Example: `/^([`<span style="color: red;">a-z0-9_\.-</span>`]+)@([`<span style="color: red;">\da-z\.-</span>`]+)\.([`<span style="color: red;">a-z\.</span>`]{2,6})$/`

Character classes match a character from a specific set. There are a number of predefined character classes and you can also define your own sets. To negate a set of characters use `^` after the first bracket and before the first character.

## The OR Operator
### Example: `/^I like (dogs`<span style="color: red;">|</span>`penguins), but not (lions`<span style="color: red;">|</span>`tigers).$/`
The example regex expression will match any of the following sentences:
- I like dogs, but not lions.
- I like dogs, but not tigers.
- I like penguins, but not lions.
- I like penguins, but not tigers.

## Flags
### Example: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`<span style="color:red;">i</span>
Expression flags change how the expression is interpreted. Flags follow the closing forward slash of the expression.

## Character Escapes
### Example: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
The backslash `\` escapes the character from any functions it could possibly have. Such as a `+`, `.`, or `[]` character.

## Author

My name is Tevis Reilly, and I am currently enrolled in MSU's Coding Boot Camp. You can see my projects on my [repo](https://github.com/tevissaur), or email me at tevisreilly1@gmail.com.
