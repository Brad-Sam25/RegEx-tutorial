# Matching Hex Values Using Regular Expression

This particular file will thoroughly explain the many aspects needed when matching a HEX value. 

## Summary

This particular regular expression is what is needed when matching HEX values:

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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
The anchor ^ can be seen as matching a position before, after, or between characters as opposed to actual characters. In other words, the caret matches the position before the first character in the string.

Example: ^b signifies that string must start with the character b such as in bcd.

The $ matches the last character in the string.

Example: d$ signifies that the string must end with the character d sucha as in bcd.

In the case of our expression for matching Hex values ^# siginifies that the first character in the string must match # and in the case of a hexadecimal number, the # is a way of determining a hexadecimal number from a decimal number. As for the $/, this signifies that the string must end with a 6 or 3. 
### Quantifiers
The quantifier identifies how many instances of a character, group, or a character class must exist in the input in order for a match to be found.

Example: /^#? in this particular case and in our expression, the quantifier is the ? and it signifies that the # can appear in the input in order for a match to be found.  

The {} quantifier determines how many instances of the particular pattern matches and this can be broken into two categories: greedy or lazy. The greedy quantifier elicits the regex engine to match as many instances of the particular patter as possible. The lazy quantifieir does the oppositie by matching the least occurrences as possible.

Example: [a-f0-9]{6}  [af0-9]{3} in this particular portion of our expression, the {3} signifies that there are 3 instances of the string in the preceeding bracket where there will be 3 characters that contain a-f and/or interger between 0-9. The same process occurs with {6} however, there are 6 characters in the string that have characters between a-f and/or intergers between 0-9. 


### Grouping Constructs
Grouping constructs act as delineations of subexpressions within a regular expression and capture substrings of an input string. This is depicted as ().

Example: ([a-f0-9]{6}|[a-f0-9]{3}) in this portion of our expression the grouping construct () is the bracket expression [a-f0-9]{6} 
 [af0-9]{3}.

### Bracket Expressions
Bracket Expressions are used to match a charcter out of a set of characters and the hyphen signifies the range of charcters.

Example: [a-f0-9] the square brackets signify matching characters that have characters between a-f and intergers between 0-9.

### Character Classes
Character Classes, otherwise known as Character Set, are used to tell the regular expression engine to compare only one out the many characters and these charcters are placed within the bracket expressions [].

Example: [a-f] in this charcter class, we are matching a single character between a and f.
### The OR Operator
The OR Operator is similar to the logical operator OR in which they are a boolean data type that match a single regular expression out of several regular expression.

Example: [a-f0-9]{6}|[a-f0-9]{3} in this portion of our expression, the | signifies that the regex engine should match with 3 characters that contain a-f and/or interger between 0-9 OR 6 characters in the string that have characters between a-f and/or intergers between 0-9. 

### Flags
In regular expressions, there may flags that impact the search and there are only 6 of them in Javascript: i (this make the search case sensitive), g (this flag looks for all matches during the search), m ( this is the multiline mode), s (this flags turns on the "dotall" mode which allows a dot to match newline character), u (This flag turns on the correct processing of surrogate pairs otherwize known as Unicode support), and y (this searches the exact position in the text otherwise know as sticky mode).

### Character Escapes
Character escapes are used to match a character having special meaning in regex and this is depicted with a backslash \.

## Author

My name is Brad and I look to become knowledgeable in as many web technologies as I possibly can and hopefully reach a level of mastery in most of the technologies both front and backend. Please feel free to view my future projects as I embark on this endeavor to mastery of most web technologies.

GitHub: https://github.com/Brad-Sam25