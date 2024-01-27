# Nested Groups Regular Expression Tutorial

Nested group regular expressions are a great way to search strings. In this tutorial we will be using an HTML <span> element as the string.

## Summary
The regular expression variable regExp will be applied to the string variable using the .match() method: 

let string = '<span class="foo">';

let regExp = /<(([a-z]+)\s*([^>]*))>/;   // THIS IS OUR REGULAR EXPRESSION

let result = string.match(regExp);
console.log(result[0]); // <span class="foo">
console.log(result[1]); // span class="foo"
console.log(result[2]); // span
console.log(result[3]); // class="my"

- Expressions: 

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

### Anchors
 ^ The caret – matches at the beginning of the text.

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
