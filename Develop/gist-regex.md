# Nested Groups Regular Expression Tutorial

Nested group regular expressions can be applied to html string searches. In this tutorial we will be using an HTML <span> element as the string.

## Summary
The nested group regular expression variable regExp will be applied to the string variable using the .match() method: 

![Expression application](<../Media/Screenshot 2024-01-29 at 11.30.16 AM.png>)

Nested Groups

Did you know parentheses can be nested? In this case the numbering also goes from left to right.

For instance, when searching a tag in <span class="foo"> we may be interested in:

- Tag content as a whole: span class="my".
- Tag name: span.
- Tag attributes: class="foo".
- Let’s add parentheses for them: <(([a-z]+)\s*([^>]*))>.

See how the regular expression is numbered below from left to right:

![RegEx](<../Media/Screenshot 2024-01-29 at 11.54.39 AM.png>)

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

 ^ The caret – matches at the beginning of the text.

### Quantifiers
 Quantifiers quantify how many times a specific part of your regular expression should be repeated.  They are needed every time you want to repeat something in a regex such as an individual character, a character class or a sub-expression.

 - "*" was used in this expression which is syntactic sugar for "{0,}" quantifier

### Character Classes
Character classes matches of the enclosed characters. In order to specify a range of characters use a '-' hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character. So keep that in mind when using hyphens.

- [a-z] matches all lower case charachters from a-z.

### Flags
Regular expressions may have flags that affect the search. There are only 6 of them in JavaScript: i, g, m, s, u, y.
- There are no flags in this expression.

### Grouping and Capturing
A capturing group groups a subpattern, allowing you to apply a quantifier to the entire group or use disjunctions within it. 
- '(...)' There are two groups in this expression.

### Bracket Expressions
Square brackets help you to define a character set, which is a set of characters you want to match.
- [^>] Negated '>' greater than character is included in this expression.

### Greedy and Lazy Match
To find a match with greedy mode, the regular expression engine uses the following algorithm:

- For every position in the string
- Try to match the pattern at that position.
- If there’s no match, go to the next position.

There are two greedy qualifiers in the reaular expression above:
- '*' means star Quantifier: 0 or more.
- '+' means plus Quantifier: 1 or more.

Lazy mode of quantifiers is an opposite to the greedy mode. It means: “repeat minimal number of times”. It is enabled by putting a question mark '?' after the quantifier, so that it becomes *? or +? or even ?? for '?'.
- There are no lazy quantifiers in this expression.

### Boundaries
Word boundary assertions checks if the current position in the string is a word boundary. A word boundary occurs when the next character is a word character and the previous character is not a word character, or vice versa. They can be expressed with '\b' or '\B'.

- There are no word boundary assertions in this expression.

### Back-references
A backreference refers to the submatch of a previous capturing group and matches the same text as that group. 
- There is no backreference in this expression.

### Look-ahead and Look-behind
A lookahead assertion "looks ahead": it attempts to match the subsequent input with the given pattern, but it does not consume any of the input — if the match is successful, the current position in the input stays the same. (?=...) or (?!...).

- There are no look ahead or behind expressions.


## Author
Yemi Ayeni - JavaScript Software Developer
- https://github.com/rehposolihpedoc/Regex

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
