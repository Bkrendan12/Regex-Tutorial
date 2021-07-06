# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

```
Anchors will match a position of the string (regex expression) whether it’s the beginning, the end, word bound or non-word bound.

^ matches the beginning of our text, and $ matches the end. Throwing ^ on the beginning of our regex and $ on the end makes it so that the text we're matching against must exactly match our regex expression, as opposed to finding it somewhere in the text.

```

### Quantifiers

```

{#} (for example, {3} or {10}) looks for that # of the preceding token. For example, if we wanted to match a phone number, we could use the regex /\d*{3}-\d*{3}-\d*{4}/ to match 3 digits, a dash, 3 digits, a dash, and 4 digits.
{#1, #2} (for example, {1,3}) looks for between #1 and #2 of the preceding token. For example, if we wanted to match between 3 and 4 digits, we could use the regex /\d{3,4}/.
+ matches at least one of the preceding token, and * matches 0 or more.

```

### Grouping Constructs

```

Capture groups are denoted by parentheses and can be referenced later in order to extract the information they enclose. For example, if we wanted to capture the first 3 digits in our earlier phone number example, we could use the regex /(\d*{3})-\d*{3}-\d*{4}/.
Class sets are groups denoted by square brackets. For example, if we wanted to match either a digit or a lower case letter, we could use the regex /[0-9a-z]/.

```

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

```

Global Flag

The g flag on a regex expression causes the regex to match every instance of the text that matches our regex. You can also just match against the first instance of text that matched our regex.

```

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
