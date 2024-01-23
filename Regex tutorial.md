# Regex - Matching an HTML Tag

Regex is a sequence of charaters that specifies a match pattern in text. Originally began in 1950 by Stephen Cole Kleene, when he formalized the concept of a regular language. 

## Summary

I will be describing /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/ which is matching an HTML tag. Of course, this just looks like someone bashed their keyboard, below will describe what the code snippet above is about. 

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


### Anchors

Caret (^) - Beginning Anchor:

The caret symbol (^) when used at the beginning of a regex pattern signifies that the pattern should match the specified content only if it appears at the start of the string.
Example: /^<([a-z]+)

Dollar Sign ($) - End Anchor:

The dollar sign ($) when used at the end of a regex pattern indicates that the pattern should match the specified content only if it appears at the end of the string.
Example: (?:>(.*)<\/\1>|\s+\/>)$/

Word Boundaries (\b):

The \b anchor is used to establish word boundaries. It ensures that the pattern matches only whole words and doesn't include partial matches within larger words.
Example: \bWORD\b

In the context of HTML tags, these anchors are often used to define the beginning and end of the tag structure. For instance, in the regex pattern /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/:


### Quantifiers

'+': Matches one or more occurrences of the preceding token.
'*': Matches zero or more occurrences of the preceding token.
'?': Matches zero or one occurrence, making the preceding quantifier optional.
'{7,9}': Forces characters between seven and nine occurrences.

### OR Operator

'|': Acts as a Boolean OR, allowing a match for either expression before or after the operator.

### Character Classes

'\w': Matches any word character (alphanumeric and underscored).
'\W': Matches any non-word character.
'\d': Matches any digit.
'\D': Matches any non-digit character.
'[A-Z]': Creates a range for uppercase letters

### Flags

Flags following the closing forward slash alter how the expression is interpreted. Examples include i for case-insensitivity and g for global matching.

### Grouping and Capturing

Parentheses '(abc){3}': Groups a selective pattern and specifies the number of repetitions.

### Bracket Expressions

Regular expressions surrounded by square brackets match a single character or collating element.

### Greedy and Lazy Match

Greedy quantifiers match as many instances as possible, while lazy quantifiers match the fewest.

### Boundaries

'\b': An anchor that establishes word boundaries, useful for "whole words only" search strings.

### Back-references

Backreferences match the same text previously matched by a capturing group, useful for capturing and referencing content within HTML tags.

### Look-ahead and Look-behind

Zero-length assertions that match characters without consuming them, allowing for advanced pattern matching.

## Author

Megan Sargent, MSU coding bootcamp student. https://github.com/mrsargent00?tab=repositories