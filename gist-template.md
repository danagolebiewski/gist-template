# REGEX Tutorial 

A regular expression is a sequence of characters that specifies a search pattern in text. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation.

## Summary

This gist will explain how to use a regular expression to validate an email address. Here is an example of using regular expression to validate the input 
^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$ 

## Table of Contents

- [REGEX Tutorial](#regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

### Anchors
Anchors are characters that define what is at the start and end of the string that is being examined. In this example the anchor is the ^ symbol at the beginning of the expression, and the $ at the end of the expression. The first anchor says that the text at the start of the string matches the expression. The beginning of the expression says to match the characters A - Z and is case sensitive, 0-9 matches characters 0-9, can have any of these symbols - ., -, +. the first and second part are added with the "@" character.  In the last part it has to match characters A-Z and is case sensitive, and characters 0-9. The {2,} part says it has to match at least 2 or more ofthe preceeding quanitifiers, and the "$" matches the end of a string.

### Quantifiers
Quantifiers are used very often. They serve as the main “building block” of complex regular expressions. In the example, the + says that it must match 1 or more tokens, and the {2,} says it has to match at least 2 or more ofthe preceeding quanitifiers. 

### Grouping Constructs
Focuses on portions of a regex pattern with parentheses so actions like quantifiers can be applied to what is inside the parentheses. In the expression ^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$, there are three groups, all seperated by parenthesis.

### Bracket Expressions
Brackets let the expression search for everything within the brackets. In the beginning of expression [A-Z0-9_.-], the brackets says that the search can be a alphabet from a to z, it can also be a number from 0 to 9, it can be a underscore, or it can be a hyphen.

### Character Classes
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. The characters are inside of brackets. In this example, [A-Z] will match all characters from A - Z, and [0-9] will return all characters 0-9. 

### The OR Operator
The "or" operator "|" allows there to be a choice in matching where the expression matches before or after is acceptable. In this example, there are no "or" operators.

### Flags
Flags are optional arguments that change the meaning of the expression pattern. Here are some examples.

"i" says to ingore capital casing so that "A" and "a" are considered the same when searching.
"g" looks for all matches when there is a search.
"m" affects "^" and "$" behavior across multiple lines when searching.
"s" enables "dotall" to match newline character. Flags were not used in this email regex.

### Character Escapes
Character escapes help to divide the escaping rules into two different lists of characters that need to be escaped:  One for characters inside a character class, and one for characters outside a character class.
Some examples are :
1) [ Purpose: Start of character class.
2) ]  Purpose: End of character class.
3) \  Purpose: Escaping.
4) '-' Purpose: Character ranges.
5) ^  Purpose: Class Negation.

Which are all used in the example. 

## Author

Dana Golebiewski
[GitHub link](https://github.com/danagolebiewski)
