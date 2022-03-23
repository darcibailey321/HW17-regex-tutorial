# Regex Tutorial

Regular expressions or "regex" for short are strings representing a pattern to be matched in a search operation.

## Summary

Regex is used for all types of programming languages. Expressions allow programers to search for specific patterns of text which can be created for just about any pattern of text that you can imagine.

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
String anchor examples:
```JS
// 	^ (caret) Matches at the start of the string the regex pattern is applied to
^. matches a in abc\ndef
// $ (dollar) Matches at the end of the string the regex pattern is applied to.
.$ matches f in abc\ndef
```

### Quantifiers
Greedy, lazy, or possessive quantifier examples:
```JS
// ? (question mark) Makes the preceding item optional. Greedy, so the optional item is included in the match if possible.
abc? matches abc or ab
// ?? Makes the preceding item optional. Lazy, so the optional item is excluded in the match if possible
abc?? matches ab or abc
```

### Grouping Constructs
Positive and negative lookahead examples:
```JS
// (?=regex) Matches at a position where the pattern inside the lookahead can be matched. Matches only the position.
It does not consume any characters or expand the match. In a pattern like one(?=two)three, both two and three have to match at the position where the match of one ends
t(?=s) matches the second t in streets.
// (?!regex) Similar to positive lookahead, except that negative lookahead only succeeds if the regex inside the lookahead fails to match.
t(?!s) matches the first t in streets.
```
Positive and negative lookbehind examples:
```JS
// (?<=regex) Matches at a position if the pattern inside the lookbehind can be matched ending at that position.
(?<=s)t matches the first t in streets.
// (?<!regex) Matches at a position if the pattern inside the lookbehind cannot be matched ending at that position.
(?<!s)t matches the second t in streets.
```

### Bracket Expressions
Brackets indicate a set of characters to match, so all characters between brackets will match.
```JS
// Any character except ^-]\ All characters except the listed special characters are literal characters that add themselves to the character class.
[abc] matches a, b or c
```

### Character Classes

```JS
// [ When used outside a character class, [ begins a character class. Inside a character class, different rules apply. Unless otherwise noted, the syntax on this page is only valid inside character classes, while the syntax on all other reference pages is not valid inside character classes.
```

### The OR Operator
Matches part of the string on either side
```JS
// | (pipe)	Causes the regex engine to match either the part on the left side, or the part on the right side. Can be strung together into a series of alternatives.
abc|def|xyz matches abc, def or xyz
```

### Flags

A flag is denoted using a single lowercase alphabetic character.
g : matches the pattern multiple times.
i : makes the regex case insensitive.
m : enables multi-line mode.
u : enables support for unicode.
s : short for single line, it causes the . to also match new line characters.


### Character Escapes

```JS
// \n, \r and \t Match an LF character, CR character and a tab character respectively
\r\n matches a Windows CRLF line break
```

## Author

Darci Bailey - Github darcibailey321

I am a developer in training with much more to learn when it comes to creating clean and efficient code, but with the help of regex it makes it easy to do.
