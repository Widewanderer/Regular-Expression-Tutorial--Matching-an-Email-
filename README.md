# Regular Expression Tutorial: Matching an Email
A Document tutorial of the Regex for an Email. Includes explanation of component parts. 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

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

Regex can be expressed literaly or by pattern. The `/` character indicates to us that this is a regex pattern rather than a literaly search. 

### Anchors

The characters `^` `$` are both anchors. These characters are used to ensure that a regex matches a string at a specific place. In Our expression, the `^` character is used to match the begining of a word or line. `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` Likewise, the `$` character marks the end of a word or line with the specified characters imediately before it.  

Example <br>
`([a-z\.]{2,6})`: specifying characters <br>
`$`: end of string <br>
`/`: end of regex <br>

### Quantifiers


### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

