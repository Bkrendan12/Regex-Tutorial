# Regular Expression Overview

```
In this overview for Regex, also known as Regular Expressions, we will go
over writing your own regular expressions that you can implement into
your own projects.
```

## Summary

```
Regex is a way of setting specific parameters the user can use when
entering into an input field. In a way, we're setting rules for the
user of what they can and cannot use in a certain input such as a form.
A good example is making sure when a user enters a phone number, we
would ask for 3 numbers, a dash, 3 more numbers, a dash and lastly,
4 numbers. This would get us the area code and the 7 digit phone number.
```

A code snippet for this example would look like:

/\d*{3}-\d*{3}-\d\*{4}/

**603-123-4567**

```

- the first group requires any 3 digits
- a dash
- the second group requires any 3 digits
- a dash
- the third group requires any 4 digits
```

A simpler code snippet example would be something as easy as:

**/tree/g**

I sat on a **_tree_** drinking a pint glass of **_tree_** vana (**treevana**)

```
Which would look for anytime the combination of the word "tree" is
used in the string/text/input. It would find the word "tree" no matter
where it is. Whether it's the word on its own or in another word such
as "treevana".
```

## Preface

```
Each example will be referring to using a Regex testing application such as:
```

[regexr.com](https://regexr.com/)

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

Anchors will match a position of the string (regex expression)
whether it’s the beginning, the end, word bound or non-word bound.

^ matches the beginning of our text, and $ matches the end. Throwing
^ on the beginning of our regex and
$ on the end makes it so that the text we're matching against must
exactly match our regex expression, as opposed to finding it somewhere
in the text.

```
Not using ^ anchors:

[1, 5, 10]
12345678910
only the 1, 5 and 10 will be allowed

Using ^ Anchors
[^1, 5, 10]
12345678910
each number other than 1, 5 and 10 will be allowed
```

### Quantifiers

Looks for that # of the preceding token.

For example:

If we wanted to match a phone number, we could use the regex

```
 /\d*{3}-\d*{3}-\d*{4}/
```

to match 3 digits, a dash, 3 digits, a dash, and 4 digits.

```
{1,3} looks for between #1 and #2 of the preceding token.
```

If we wanted to match between 3 and 4
digits, we could use the regex

```
/\d{3,4}/.+ matches at least one of the preceding token, and \* matches 0 or more.
```

### Grouping Constructs

```
Capture groups are denoted by parentheses and can be referenced later
in order to extract the information they enclose. For example, if we
wanted to capture the first 3 digits in our earlier phone number example,
we could use the regex /(\d*{3})-\d*{3}-\d*{4}/. Class sets are groups
denoted by square brackets. For example, if we wanted to match either
a digit or a lower case letter, we could use the regex /[0-9a-z]/.
```

### Character Classes

Character classes are only used for finding
digits \d, whitespace \s and words \w

\d **digits** [0-9] includes all digits from all scripts
\w **wordcharacter** [A-Za-z0-9_] matches the ASCII characters
\s **whitespace** [\t\r\n\f] matches space, a tab, a carriage return, a line feed

```
Example of digits /d:

[0-9] is the same as \d
```

### Bracket Expressions

```
A bracket expression is a list of characters enclosed by [brackets].
It matches any single character in that list. If the first character
of the list is the ‘^’ symbol, then it matches any character not in
the list. The regular expression ‘[0123456789]’ matches any single
digit. A hyphen creates a range, and a caret at the start negates
the bracket expression.
```

### The OR Operator

OR is a logic term used to provide selection choice from multiple
choices. If we want to look for specified words we set in the regular
expression, we can place 3 words for example inside of parentheses
split with the "|" symbol saying "we are looking for this word or
this word or this word".

Regular Expression:

```
* /(red | blue | yellow)
```

Test string:

```
* I like the color red
* I like the color blue
* I like the color green
```

Only the word red and blue will be highlighted. Green won't be
highlighted because we didn't include it in our regular expression.

### Flags

```
These are tokens that modify the behavior of searching. We can use these to make it a search in a different way.

some popular examples of flags include:

- Ignore Casing "/i" Makes an expression search case-insensitive.
- Global "/g" Makes an expression search for all occurrences.
- Dot All "/s" Makes the wild-character "." match new lines as well.
- Multiline "/m" Makes the boundary characters "^" and "$" match
  the beginning and ending of every single line instead of the beginning
  and ending of the whole string.
```

### Character Escapes

```
Character Escapes are used with backslashes. It's easy at first to think you
only use the backslash to ESCAPE something in a search but you also use it to
"bring" so the character escape will bring and escape. In order to use a
literal backslash anywhere in a regex, it must be escaped by another backslash.

There are several characters that need to be escaped to be taken literally (at least outside char classes):

* Brackets: []
* Parentheses: ()
* Curly braces: {}
* Operators: *, +, ?, |
* Anchors: ^, $
* Others: ., \

In order to use a literal ^ at the start or a literal $ at the end of a regex, the character must be escaped.
```

## Author

This Overview on **_Regular Expressions_** was written by myself, Brendan Kurylo,
a junior web developer from Southern New Hampshire.

You can find a copy of the .gist version at my github at:

**[Regular Expressions .gist](https://github.com/Bkrendan12/Regex-Tutorial/blob/master/gist-template.md)**

**[Regular Expressions git repo](https://github.com/Bkrendan12/Regex-Tutorial)**

**[My Github](https://github.com/Bkrendan12)**
