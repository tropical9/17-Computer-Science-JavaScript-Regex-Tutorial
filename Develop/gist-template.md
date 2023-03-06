# REGEX Tutorial

This is a Regex tutorial that covers Matching an Email 

` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ `

## Summary

Regular expressions or regex, are a powerful tool for pattern matching and text processing. It is a valuable skill to learn as they are universal and used within all programming languages. This tutorial will cover how matching an email expression works.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ `

Breakdown of the patterns into individual components:

1. `/^` - This is the beginning of the pattern and matched the start of the string.
2. `([a-z0-9_\.-]+)` - This is the first capturing group and matches one or more lowercase letters (a-z), numbers(0-9), underscores (_), dots (.) or hyphens (-). This represents the username portion of an email address.
3. `@` - This matches the "@" symbol, which separates the username from the domain name. 
4. `([\da-z\.-]+)` - This is the second capturing group. This matches one or more digits, lowercase lettersm dots or hyphens. This represents the domain name. 
5. `\.([a-z\.]{2,6})` - This is the third capturing group. This matches a period followed by two to six lowercase letters or perios. This represents the top-level comain name such as .com, .net, .org, etc.
6. `$` - This matches the endinf of rhe string. 

```
Examples:

    Match: 
        john.doe@email.com
        john_doe1@email.email.co.us
    Invalid Match:
        john.doe@com
        john.doe@email..com
  ```


### Anchors

1. `^` - The regex pattern starts with this anchor.
2. `$` - The regex pattern ends with this anchor.

This ensures that the entire string matches the pattern entirely.

### Quantifiers

1. `+` - This symbol means "one or more occurrences of the previous character or group."

In this case, this is used to match one or more characters in the username and domain name sections of the email address.

### OR Operator

1. `|` / OR operator - This symbol is called the OR operator, and it allows you to specify multiple alternatives for a pattern. 

This is not used in this particular expression. 

### Character Classes

1. `[]` brackets- This bracket is used to define a character class, which matches any single character that is contained within the brackets. 

We have used character classes to match lowercase letters, digits, underscores, dots and hyphens.

### Flags

Not used in this expression.

Examples: g - global matching, i - case-insensitive matching, m - multiline matching.

### Grouping and Capturing

`()` - This is used to group and capture parts of the pattern.

We have used three groups that capture the username, domain name, and top-level domain of the email address.

### Bracket Expressions

`\d` - This expression is used to marched any character that is contained within them. This matches any digit character and "." which matches any character except for newline.

### Greedy and Lazy Match

1. `+` - This quantifier is by default a greedy quantifier, meaning it will match as many characters as possible.

### Boundaries

Not used in this expression.

Examples: \b - word boundary, \B - non-word boundary.

### Back-references

Not used in this expression.

Denoted by the backslash "\" followed by the group number. This allows you to refer to a previous captures group in the pattern. 

### Look-ahead and Look-behind

Not used in the expression.

The match a position in the string without consuming any characters. 
They are denoted by: `(?= )` - positive look ahead.
                     `(?<= )` - positive look behind.
                     `(?! )` - negative look ahead.
                     `(?<! )` - negative look behind.

## Author

Sharmaine Pineda

https://github.com/tropical9

