# Regex-Tutorial

Regex (Regular Expression) is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or find and replace a character or sequence of characters within a string. They are also used frequently to validate input data. Example: Regular Expression (Regex) can be used for Emails by creating and checking if the email is properly created.

## Summary

The purpose of this tutorial is to help users understand and define the sequence of special characters to verify a search term. This tutorial will explain the use of regex to match emails using the expression 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. 
This process can be useful when validating emails using applications such as Node (Inqurier) or MongoDB.

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Componets

### Anchors
Anchors have special meaning in regex. They do not match any character. Instead they match a position before or after characters:

 ^ – The caret anchor matches the beginning of the text.
 $ – The dollar anchor matches the end of the text.

### Quantifiers
There are two quantifiers used in this regex. The first + which is identified as a greedy quantifier. This quantifier will allow connection for te users email+ email service + .com. The other quantifier is the {2,6}, this will match everything after the . 2-6 times to ensure it has a minimum of 2 characters and a maximum of 6. 

### Grouping Constructs
The first group ([a-z0-9_\.-])+ will capture the email name, the second group ([\da-z\.-]+) will capture the users email provider and the third group ([a-z\.]{2,6}) will capture the top level domain input from the user. 

### Bracket Expressions
A bracket expression is a list of characters enclosed by ‘[’ and ‘]’. It matches any single character in that list. If the first character of the list is the caret ‘^’, then it matches any character not in the list, and it is unspecified whether it matches an encoding error. For example, the regular expression ‘[0123456789]’ matches any single digit, whereas ‘[^()]’ matches any single character that is not an opening or closing parenthesis, and might or might not match an encoding error.

Bracket expressions within the email validation are within the []. 
In the first group of the regex ([a-z0-9_\.-]+) everything within the [] is going to match any letter a-z, any number from 0-9 and the characters _ . - . This regex has 3 sets of bracketed expressions each requiring different pieces of information. 

### Character Classes
The character class is the most basic regex concept after a literal match. It makes one small sequence of characters match a larger set of characters. For example, [A-Z] could stand for any uppercase letter in the English alphabet, and \d could mean any digit.

### The OR Operator
OR operator is to match the characters on the left or the right of the operator, essentially serving as an or, as in and/or. 

Using the | as in m|M would match either m or an M from the string. For example if you use https?:\/\/(www\.)?[\d-a|A it would search or a OR A. 

### Flags
A flag is an optional parameter to a regex that modifies its behavior of searching. A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.

Flag Expressions:

i: Ignores casing. Makes expression case-sensitive
g: Global. Makes expression search for all occurrences
s: Dot All. Makes the wild characters . match newlines as well
m: Multiline. Makes boundary characters ^ and $ match beginning and end of every line.
y: Sticky. Indicates that it matches only from the index indicated by the lastIndex property of this regular expression in the target string (and does not attempt to match from any later indexes)
u: Unicode. Expression assumes individual characters are code points, not code units and will then match 32 bit characters.

### Character Escapes

The backslash in a regular expression precedes a literal character. You also escape certain letters that represent common character classes, such as \w for a word character or \s for a space. The following example matches word characters (alphanumeric and underscores) and spaces.

Escaped Characters

\\    single backslash

\A    start of a string

\b    word boundary. The zero-length string between \w and \W or \W and \w.

\B    not at a word boundary

\cX   ASCII control character

\d    single digit [0-9]

\D    single character that is NOT a digit [^0-9]

\E    stop processing escaped characters

\l    match a single lowercase letter [a-z]

\L    single character that is not lowercase [^a-z]

\Q    ignore escaped characters until \E is found

\r    carriage return

\s    single whitespace character

\S    single character that is NOT white space

\u    single uppercase character [A-Z]

\U    single character that is not uppercase [^A-Z]

\w    word character [a-zA-Z0-9_]

\W    single character that is NOT a word character [^a-zA-Z0-9_]

\x00-\xFF  hexadecimal character

\x{0000}-\x{FFFF}   Unicode code point

\Z    end of a string before the line break

## Author
AKeia M.

Junior Software Engineer completing requirements for Bootcamp.
 GitHub profile (https://github.com/DrMcCollum5)
