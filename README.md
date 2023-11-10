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

Example 
`([a-z\.]{2,6})`: specifying characters <br>
`$`: end of string <br>
`/`: end of regex <br>

### Quantifiers
Quantifiers in regular expressions are symbols or meta-characters used to specify the number of times a particular character, group of characters, or pattern can appear in a string. They control the repetition of elements within the regular expression, allowing you to match a specific quantity or a range of quantities of characters or patterns.

In our example the character `+` is used after our bracket expressions to search for the specification within the bracket expression one or more times.

Example: 
`/^([a-z0-9_\.-]+)` [ search for lowercase letters, digits, underscores, hyphens, or periods ] `+` occuring one or more times. 

### Grouping Constructs

### Bracket Expressions
Square brackets `[ ]` represent a range of characters we want to match. This is called a bracket expression. Our email regex begins with 
`/^([a-z0-9_\.-]+)`. <br>
The code <br>
`[a-z]` specifies that we want to search for any letter from A-Z.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

