# Regex Tutorial: Matching a hex value

This tutorial will explain how a specific Regex (regular expression) works, how is it built and what every section of it is doing.

## Summary

The Regex I'm going to explain is used to check if the targeted value is matching a hexadecimal value. A hexadecimal value is a
number system that uses 16 unique symbols (0-9 and A-F). 
An example of such a "hex value" is: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The Anchors we're encountering in the Regex we're explaining are `$` and `^`.
Anchors have special meaning in Regex. They do not match any characters but they match a position.

- `^` matches the beginning of the text
- `$` matches the end of the text.

The above Regex starts with `/^#` and it means that the value checked to match a hex number should start with `#`.


### Quantifiers

Quantifiers are used to specify the number of instances of a character or group should be part of the input.
In the Regex we are going through today we have this snippet `#?` in which we encounter the `?` quatifier.

- `?` it is a greedy quantifier and it is used to make the preceeding item optional. In the above case, the `?` is preceeding the `#` making it optional.

- `{n}` is a quantifier tht specifies the number of times the character or characters that are in front of the braces are found in the vealue that we're searching in.

### Grouping Constructs

Grouping constructs are used to treat multiple characters as a single unit. In the above example we encounter several grouping constructs such as:

- `(a|b)` gives us a choice of either the first item in the brackets or the second item. In our example regex we have a choice of either `[a-f0-9]{6}` or `[a-f0-9]{3})`.

There are no other exqamples of Grouping Constructs in our chosen Regex.

### Bracket Expressions
The square brackest `[]` that we find in a bracket expression are used to declare a range. You can find the example below.

- `[abc]` is declaring a range. In the regex for matching a hex value we encounter it in the next example `[a-f0-9]`. In this case, the value has to match either a letter from `a-f` or a number from `0-9`. Ranges are inclusive.

### Character Classes

A character class is used to instruct the regex engine to match only one of several characters. In our Regex above we encounter a character class: `[a-f0-9]`. In this example it will match a singe hexadecimal digit, lowercase sensitive. 

In this case the order of the characters does not matter.

### The OR Operator

The OR Operator is represented by the pip character `|`. This item separates the terms in each group. In our above example we encounter `([a-f0-9]{6}|[a-f0-9]{3})` which translates into `([a-f0-9]{6} OR [a-f0-9]{3})`.

### Character Escapes

The character escapes are used to escape a character that has a special meaning inside a regular expression. To escape a character in a Regex we need to preceed it with the `\` character.

## Author
My name is Dylan Bittikofer, My github profile is https://github.com/Dylanbitto feel free to look at my projects.