# Matching an Email using Regex

In this tutorial we will go over how to form a regular expression that can identify any correctly formatted email.
We will identify the regular expression that does the job and go over some of its components.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Below is the regular expression that is used to identify valid email address.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

It consists of a variety of characters that don't immediately make sense. We will go into detail into what each of these 
characters, symbols and character groups mean. 
The first thing to know is that the first and last symbol are used to delimit the beginning and end of the regular expression. We'll now go into details on the mechanics of this regular expression.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
In the above email regex, we have the following components: anchors, quantifiers, or operators, character classes,
flags, grouping, bracket expressions and greedy match. These are all discussed in detail in the the sections below.
* means 0 or more of a match
+ means 1 or more of a match
? means 0 or 1

### Anchors
Anchors are used to tell the program the position of the character that is being matched. In our email regex, the '^'
symbol specifies that the result matched by the following group must be found at the begining of the string. Also, the
'$' symbol specifies that the preceeding pattern is found explicitly at the end of the string.
A simpler example is '/^a\w/z$/' that specifies any word that starts with an 'a' and ends with a 'z'.

### Quantifiers
Quantifiers allow the regex to scale by specifying the number of matches to expect. 
This snippet of the email regex '[a-z0-9_\.-]+' indicates that there can be one or
more matches from the result of the bracket

### OR Operator
There are two types of or operators: the '|' and the '[]' symbols. In the email regex, the '[]' symbol has been used.
In our regex we have, '[a-z0-9_\.-]' as an example. From left to right, it can be explained to succeed when matching: characters 'a' to 'z',
or digits '0' to '9' or an underscore or a period or a hyphen.

### Character Classes
There are three character classes, two of which have been used in the email regex.
\w - matches any character from 'a' to 'z' (uppercase and lowercase) and digits 0 - 9
\d - matches digits from 0 - 9
\s - matches space characters

### Flags
The beginning and ending '/' mentioned ealier that are used to mark the start and end of the regex are known as flags.

### Grouping and Capturing
The '()' characters are used to group patterns in order to reference them later or apply common operations to the group.
An example is '^([a-z0-9_\.-]+)'. The '^' applies to anything matched by the pattern in the brackets. This is possible 
thanks to the grouping feature of regular expressions.

### Bracket Expressions
Bracket expressions '[]' can be used as a an or operator. This has been explained earlier in the 'Or Operator' section.

### Greedy and Lazy Match
Greedy match refers to symbols that allow unlimited number of repetitive matches. The '*' and '+' are greedy match expressions
since they match 0 and 1 or more characters. Lazy match is where only one or more characters are matched. The '?' is a lazy match.

## Author

Adisa Bello is an up and coming web developer. A link to the author's GitHub profile (https://github.com/adisabello/Unique-Regex-Tutorial)
 