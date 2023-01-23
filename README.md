# Let-me-tell-you-about_Regex

Regex (short for Regular Expression) is a sequence of characters that forms a search pattern. It is used to match or find specific strings or sets of strings, mainly in text processing. Regex is supported by many programming languages, including Python, Java, C++, and JavaScript. It can be used for tasks such as searching, editing, and manipulating text, validation of input, and more.

## Summary

A Regex proves useful in matching a URL in order to locate special text patterns. Like in a password.
```
https?:\/\/(www\.)?[\d-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)
```
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
These are used to anchor the pattern to a specific position in the string. `^` is used at the beginning, while `$` used at the end. When validating a password anchors can be used to ensure that certain criteria are met.

For example, the `^` anchor can be used to ensure that a password starts with a specific character or set of characters. A regex pattern of `^[A-Z]` would ensure that the password starts with an uppercase letter.

Also, the `$` anchor can be used to ensure that a password ends with a specific character or set of characters. For example, a regex pattern of `[0-9]$` would ensure that the password ends with a digit.

You can also use both anchors together to check for a full string match for the pattern. This is useful for validating a password that has a specific format. The pattern `^(?=.[a-z])(?=.[A-Z])(?=.*\d)[a-zA-Z\d]{8,}$` would ensure that the password has at least 8 characters with at least one lowercase letter, one uppercase letter and one digit.

### Quantifiers
These are used to specify the number of times a character or group of characters can occur in a pattern. When validating a password quantifiers can be used to ensure that certain criteria are met.

For example, the `+` quantifier can be used to ensure that a password contains at least one or more of a specific character or set of characters. The regex pattern of `^(?=.*[a-z])+` would ensure that the password contains at least one lowercase letter.

### OR Operator
The OR operator, represented by the "|" symbol, is a metacharacter used to match one of several possible patterns. When validating a password the OR operator can be used to ensure that a password meets one or more of a set of criteria.

For example, you could use the OR operator to ensure that a password contains at least one of several different characters or character classes. The regex pattern `^(?=.*[a-z]|[A-Z]|\d)` would ensure that the password contains at least one lowercase letter, one uppercase letter, or one digit.

### Character Classes
These are represented by square brackets and are used to match any character from a set of characters. When validating a password character classes can be used to ensure that a password meets specific criteria.

For example, you could use character classes to ensure that a password contains at least one lowercase letter, one uppercase letter, and one digit. The regex pattern `^(?=.[a-z])(?=.[A-Z])(?=.*\d)` would ensure that the password contains at least one lowercase letter, one uppercase letter, and one digit.

### Flags
These are used to specify various options that can affect the behavior of the regex pattern. When validating a password flags can be used to modify the behavior of the regex pattern.

For example, the `i` flag makes the regex pattern case-insensitive, meaning that the pattern will match both uppercase and lowercase letters. The regex pattern `^(?=.*[a-z])` with the "i" flag would match the password "PaSsWoRd", even though it contains only uppercase letters. The "m" flag makes the `^` and `$` anchors match at the beginning and end of a line, not just the entire string. And the "s" flag makes the dot metacharacter match any character including newline.

### Grouping and Capturing
These are used to group characters and capture their match. When validating a password grouping and capturing can be used to apply quantifiers to the entire group, or refer to the captured text later in the pattern or in the replacement text.

For example, when you want to match a password that contains at least one digit, one uppercase letter, and one lowercase letter. You could use grouping and capturing to group the digit, uppercase letter, and lowercase letter together and apply the `+` quantifier to the group. The regex pattern `^(?=.(?=\d)(?=.[A-Z])(?=.*[a-z]))` would match the password "PassWord1".

### Bracket Expressions
These are also called character classes or character sets. When validating a password they can be used to ensure that a password meets specific criteria.

For example, you could use a bracket expression to ensure that a password contains at least one lowercase letter, one uppercase letter, and one digit. The regex pattern `^(?=.[a-z])(?=.[A-Z])(?=.*\d)` would ensure that the password contains at least one lowercase letter, one uppercase letter, and one digit.

### Greedy and Lazy Match
These refer to the way that a quantifier (such as * or +) matches the preceding character or group of characters. When validating a password they can be used to ensure that a password meets specific criteria. 

A greedy match, which is the default behavior, will match as many characters as possible while still allowing the overall regex pattern to match. The regex pattern `.*` would match any number of characters, including the entire input string.

A lazy match matches as few characters as possible while still allowing the overall regex pattern to match. The regex pattern `.*?` would match the smallest possible string that still allows the overall regex pattern to match.

### Boundaries
These are used to specify the position of a pattern within a string. They are represented by special characters such as `^`, `$`, `\b`, and `\B`. When validating a password they can be used to ensure that certain criteria are met.

The `^` boundary can be used to ensure that a password starts with a specific character or set of characters. A regex pattern of `^[A-Z]` would ensure that the password starts with an uppercase letter.

The `$` boundary can be used to ensure that a password ends with a specific character or set of characters. A regex pattern of `[0-9]$` would ensure that the password ends with a digit.

The `\b` boundary can be used to match the position between a word character and a non-word character. 

The `\B` matches the position of a specific word in a string.

### Back-references
These are used to match the same text as previously matched by a capturing group. They are represented by a backslash `\` followed by the group number. When validating a password they can be used to ensure that certain criteria are met. 

For example, you could use a back-reference to ensure that a password contains a specific character or set of characters twice in a row. The regex pattern `^([a-z])\1` would match a password that contains two consecutive lowercase letters.

### Look-ahead and Look-behind
These are used to check for the presence of a pattern without consuming any characters. They are represented by the special constructs `(?=...)` and `(?<=...)`. When validating a password they can be used to ensure that certain criteria are met.

You could use a positive look-ahead to ensure that a password contains at least one lowercase letter, one uppercase letter, and one digit. The regex pattern `^(?=.[a-z])(?=.[A-Z])(?=.*\d)` would ensure that the password contains at least one lowercase letter, one uppercase letter, and one digit.

You can use a look-behind to match a password that starts with a digit and contains at least one uppercase letter. To do this you can use the pattern `(?<=^\d)(?=.*[A-Z])`.

## Author
Sue is an aspiring Full-Stack Developer.

[subie23](https://github.com/subie23)

