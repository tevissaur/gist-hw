# Regex Tutorial: Matching an email address

Ever wondered how the following jumble of characters:
    `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
is able to find an email inside of a string? 
Here in this tutorial, I will breakdown this regular expression and explain how each regex function operates. 
## What is a regular expression?

It is a sequence of characters that defindes a specific pattern. When included in code, regular expressions are used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also handy in trying to validate input.

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
### Example: <span style="color:red">/^</span>`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. This matches a position, not a character.
## Quantifiers
### Example: `/^([a-z0-9_\.-]`<span style="color:red;">+</span>`)@([\da-z\.-]`<span style="color:red;">+</span>`)\.([a-z\.]`<span style="color:red;">{2,3}</span>`)$/`


## Grouping Constructs
### Example: `/^`<span style="color: red;">([a-z0-9_\.-]+)</span>`@`<span style="color: red;">([\da-z\.-]+)</span>`\.`<span style="color: red;">([a-z\.]{2,6})</span>`$/`

## Bracket Expressions
### Example: `/^(`<span style="color: red;">[a-z0-9_\.-]</span>`+)@(`<span style="color: red;">[\da-z\.-]</span>`+)\.(`<span style="color: red;">[a-z\.]</span>`{2,6})$/`

## Character Classes
### Example: `/^([`<span style="color: red;">a-z0-9_\.-</span>`]+)@([`<span style="color: red;">\da-z\.-</span>`]+)\.([`<span style="color: red;">a-z\.</span>`]{2,6})$/`

## The OR Operator
### Example: `/^I like (dogs|penguins), but not (lions|tigers).$/`
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

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
