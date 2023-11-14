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
- [Character Escapes](#character-escapes)
- [Breakdown](#breakdown)

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

Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In our example the character `+` is used after our bracket expressions to search for the specification within the bracket expression one or more times.

Example: 
`/^([a-z0-9_\.-]+)` [ search for lowercase letters, digits, underscores, hyphens, or periods ] `+` occuring one or more times.

The construction of curly brackets `{ , }` is also a common quantifier. In the Url regex it apears near the end of our code. `([a-z\.]{2,6})$/ `  <br>
`{2,6}` indicates that we are looking for between 2 and 6 of the proceeding specifications `[a-z\.]` <br>

### Grouping Constructs
Grouping constructs are used to group together one or more characters, subpatterns, or elements so that you can apply quantifiers or operators to them as a whole. The primary way this is done is using the parentheses `( )` 

Our expression has 3 grouping constructors : <br>
 /^`([a-z0-9_\.-]+)` @ `([\da-z\.-]+)` \ . `([a-z\.]{2,6})` $/

 `([a-z0-9_\.-]+)` : The 1st caputure group is for the first part of our email adress. (everything before the `@` character) `a-z0-9_\. -`  specifies the regex to allows lowercase letters, digits, underscore, period, and hyphens. The `+` quantifier specifies that one or more of these characters is needed.

`([\da-z\.-]+)` : The 2nd capture group is the domain adress. `/d` stands for any diget 0-9, `a-z` for any lowercase letter, \ . for a period, `- ` for a hyphen. 

`([a-z\.]{2,6})` : The 3rd capture group is used to match a top level domain (TLD) `[a-z\.]` allows for lowercase letters and periods and `{2,6}`is a quantifier specifying that the TLD is between 2 and 6 characters long. 

### Bracket Expressions
Square brackets `[ ]` represent a range of characters we want to match. This is called a bracket expression. Our email regex begins with 
`/^([a-z0-9_\.-]+)`. <br>
The code <br>
`[a-z]` specifies that we want to search for any letter from A-Z with the hyphen `-` indicating range.

### Character Escapes
Character escapes are a sequence of characters used to represent special meanings. Most special characters begin with a backslash `\` followed by a second character. <br>
Examples: <br>
`\d` Matches any digit <br>
`\s` Matches any whitespace Character <br>


The 2nd use of Character Escapes is to show symbols which otherwise could not be show as literals. Such  `\.` to represent a period. This is used in our expression to represent the 'dot' of '.com' or '.edu' as well as allow for periods within 2 or the grouping constructs. 

### Breakdown 
Full Email Regex: `/^([a-z0-9_\ .-]+)@([\da-z\ .-]+)\ .([a-z\ .]{2,6})$/`

`/` Begining of regex <br>
`^` Anchor: start of line <br>
`([a-z0-9_\.-]+)` Capture group: Username: matches one or more lowercase letters, digits, underscores, periods, or hyphens. <br>
`@` literal <br>
`([\da-z\.-]+)` Capture Group: Domain Name: one or more digits, lowercase letters, periods, or hyphens. Character Escape representing literal period. <br>
`\.` Character Escape: literal period. ('dot' in .com) <br>
`([a-z\.]{2,6})` Capture group: Top domain: Character class that matches lowercase letters or periods followed by quantifier specifying between 2 and 6 characters.
`$` Anchor: Entire string must mach pattern start to finish <br>
`/` End of regex <br>

## Author
This readme was created by Slava Tyson Trotz. 

GitHub of Magos Slava
https://github.com/Widewanderer/


