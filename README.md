# Email verification

The purpose of this tutorial is to explain Regex (regular expression) and the components. A regex is a sequence of characters that forms a search pattern. It can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string.
## Summary

This tutorial explains the different components on how to use regex to match email addresses using:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
For regex, anchors are the symbols displayed at the beginning and ending of the string. The (^) is the opening anchor that matches the beginning of input and the ($) matches the ending anchor of the input. The code inside the opening and closing anchors includes a combination of lower case letters, numbers, underscores, periods, and hyphens.

### Quantifiers
Quantifiers are characters that describe numeric limits that characters or groups can have when matching with regex. In the above example, there are two quantifiers in this regex ( +, {2,6}). The (+) matches the preceding character grouping (encapsulated by []) one or more times. The {2,6} quantifier matches the preceding character grouping from 2 to 6 times.

### Grouping Constructs
Grouping constructs are used to capture a matched a pattern within an input. Grouping is done through the use of (). In our example, we are using ([a-z0-9_.-]+) in order to group the pattern we are expecting from the first character of the input. Additionally, the ([\da-z.-]+) and ([a-z.]{2,6}) are used to match inputs after the @ and ., respectively.

### Bracket Expressions
Bracket expressions are identified by the characters within the brackets []. Each set of brackets can have any number of characters that it can be matched to and this is done by settings ranges of characters that include letters, numbers, and special characters such as:

a-z: All lower case letters from a to z
A-Z: All upper case letters form A to Z
0-9: All numerical digits from 0 to 9
-: Hyphen
_: Underscore
.: Period
### Character Classes
Character classes is a special notation that matches the characters from a regex within the bracket. Character classes can refer to a specific range of characters, or a specific, single character. In the above email regex, the character class is [\da-z.-].

### The OR Operator
Character escapes are identified through the use of . They are a necessary addition within the regex as they allow the use of other specific symbols that could have other use/meaning. In the above example, a (.) is used; however, for a literal period to be used in the string it will have to be written as ., as it "escapes" in order for the regex to denote the real use of a period.

### Flags

Flags can change how the expression is interpreted. Flags follow the closing forward slash of the expression.

Please see below for the common example of flags:

i ignore case: make the entire expression case-sensitive.
g global search: store the index of the last match.
m multiline: cause the beginning and end anchors to match the start and end of a line instead of the whole string.
s dotall: causes dot(.) to match any character.
y sticky: will only match from its last index position and ignores the global search flag.
Character Escapes

### Character Escapes
The backslash in regex escapes a character. For example, in this tutorial, \. is used to separate the email host name and domain. The reason for this is because dot(.) will be interpreted as character class where it will try to match any character except line breaks as I mentioned in Character Classes section. Because of this, you want to add backslash () to avoid that happening.

Regex for an email: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/.
## Author

My name is rammohan and I am currently a student at adelaide Coding Bootcamp. Feel free to contact me via the following methods:

github :https://github.com/rammohanmiryala/email_verification.git 
