# Regular Expression (Regex) Tutorial: Matching a Hex Value

In this tutorial i am going to explain regular expressions most commonly reffered to as regex. I am going to breakdown some of the most comonly used characters for you. A Regex is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also used frequently to validate input data.

## Summary

Software developers and system designers widely use hexadecimal numbers because they provide a human-friendly representation of binary-coded values. The code snippet to find a hex value that I will breakdown for you is:
```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

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
Anchors are a different breed. They do not match any character at all. Instead, they match a position before, after, or between characters. They can be used to “anchor” the regex match at a certain position.

Anchors in our expression for example are:
<br>

- `^` indicates the beginning of an expression.
- `$` indicated the end of an expression.

### Quantifiers
Quantifiers match a number of instances of a character, group, or character class in a string.

Quantifiers in our expression for example are:
<br>

- `{6}` and `{3}` think of these as a multiplyers. So we are multiplying `[a-f0-9]` by 6 and again by 3.

### Grouping Constructs
Grouping constructs delineate subexpressions of a regular expression and typically capture substrings of an input string.

A Grouping Construct in our expression for example is:
<br>

- `[a-f0-9]` this is searching for lowercase values a-f and/or values 0-9. 

### Bracket Expressions
Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set. Remember that these character sets are case sensitive, unless you set the `i` flag.
<br>
Bracket Expressions in our expression for example is:
<br>

- `[a-f0-9]` You will often see ranges of the alphabet and/or all numerals.

### Character Classes
Character classes distinguish kinds of characters such as, for example, distinguishing between letters and digits. A character class. Matches any one of the enclosed characters. You can specify a range of characters by using a hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character.
<br>

Character Classes in our expression for example is:
<br>

- `[a-f0-9]` `a-f` searches for letters a-f while `0-9` searches for digits 0-9.

### The OR Operator
In a regular expression it is denoted with a vertical line character `|`. Think of it as a literal OR in a sentance. 

The OR Operator in our expression for example is:
<br>

- `[a-f0-9]{6}|[a-f0-9]{3}` so think of it as `[a-f0-9]{6}` "OR" `[a-f0-9]{3}`.

### Flags
A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character. In JavaScript regex, we have a total of 6 flags, each serving a different purpose. Note there are no flags in our expression.
<br>

The 6 flags are as follows:
- `i`	Ignore Casing	Makes the expression search case-insensitively.
- `g`	Global	Makes the expression search for all occurrences.
- `s`	Dot All	Makes the wild character . match newlines as well.
- `m`	Multiline	Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
- `y`	Sticky	Makes the expression start its searching from the index indicated in its lastIndex property.
- `u`	Unicode	Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.

### Character Escapes
Note, we are not using any character escapes in our expressions, but I will cover some that are often used.
<br>  

The backslash `\` in a regular expression indicates one of the following:

- The character that follows it is a special character.For example, `\b` is an anchor that indicates that a regular expression match should begin on a word boundary, `\t` represents a tab, and `\x020` represents a space.

- A character that otherwise would be interpreted as an unescaped language construct should be interpreted literally. For example, a brace `{` begins the definition of a quantifier, but a backslash followed by a brace `\{` indicates that the regular expression engine should match the brace. Similarly, a single backslash marks the beginning of an escaped language construct, but two backslashes `\\` indicate that the regular expression engine should match the backslash.

## Author

Hello, my name is Sarah Lang. Thank you for reading my tutorial! : )<br>
To see more checkout my [GitHub](https://github.com/sarahlang9800) 