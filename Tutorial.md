# REGEX TUTORIAL

## Summary
Regular expressions, or regex for short, are a series of special characters that define a search pattern.

This tutorial explains a regular expression (regex): 

```
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 
```

The expression allows us to search for emails.

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
A regex is considered a literal, so the pattern must be wrapped in slash characters (/).

### Anchors
The characters ^ and $ are both considered to be anchors.

The ^ anchor signifies a string that begins with the characters that follow it.
The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.

```
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

The string starts after the ^ anchor and ends before the $ anchor.
```

### Quantifiers
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for.

```
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

{2,6} 
This quantifier means that this string has to be between 2 and 6 characters.
```

### OR Operator
A bracket expression does not require the string to meet all of the requirements in the pattern.


### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match.

```
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

\d  Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9]
```

### Flags
Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex.

### Grouping and Capturing
The primary way you group a section of a regex is by using parentheses (()). Each section within parentheses is known as a subexpression.

Capturing groups capture the matched character sequences for possible re-use (including a numbered backreference) while non-capturing groups do not. A grouping construct can be made non-capturing by adding the characters ?: at the beginning of an expression inside the parentheses.

```
([a-z0-9_.-]+) for the first part of the email
([\da-z.-]+) gets the domain name
([a-z.]{2,6}) for the .com

+ is a connector between all the grouped strings
[a-z0-9_.-] looks for characters that match a-z and 0-9 characters; 
[\da-z.-] looks for characters that match a-z, (.), and (-) characters; 
[a-z.] looks for characters that match a-z and (.) characters

```

### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match.

### Greedy and Lazy Match
Greedy quantifiers will match as many occurrences of particular patterns as possible. 

Lazy quantifiers will match as few occurrences as possible.

## Credits
Christopher L. Cristóbal Zayas (cl-czayas)