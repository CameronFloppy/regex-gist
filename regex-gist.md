# Regular Expressions

Regular expressions, or regex, are a sequence of characters that defines a set of search parameters. They are extremely versatile and customizable, so they are an important tool for any developer to know how to use.

## Summary

The regex we are going over today is, /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ . This is the regex for matching a hex value.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
There are 2 anchors in this expression, ^ and $. The ^ at the beginning says that the value must begin with the following character or string, so in this case it is saying that it must begin with #. The $ at the end says that the value must exactly match the preceding parameters. 
### Quantifiers
This regex contains 2 quatifiers, {6} and {3}. These denote the number of times we want to match the preceding bracketed expression. 6 would be the length of any standard hex value, and any hex value that has 3 characters that repeat, such as #ffcc99 can be represented with 3 digits.
### OR Operator
The OR operator in this expression, |, means that the value we are looking to match must be either [a-f0-9]{6} or [a-f0-9]{3}.
### Bracket Expressions
With in this regex the same bracketed expression is repeated twice, [a-f0-9]. A bracketed expression will accept any value in any of the ranges contained within it, in this example any letter from a to f in the alphabet and and number from 0 to 9 would be accepted.
### Greedy and Lazy Match
This regex contains ? which is a lazy match quantifier, this essentially means that there should be at most 1 of the preceding value, which in this case is #.
## Author

This was written by Jay Ford https://github.com/jayford45
