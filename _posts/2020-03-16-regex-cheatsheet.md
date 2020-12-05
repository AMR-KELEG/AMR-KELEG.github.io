---
layout: post
title: My regex cheatsheet
date: 2020-03-16
description: A set of regex related tips/concepts
---

Regular expressions are widely used in detecting text patterns. In this post, I will summarize my list of tricks and common regex that I find useful.

## Basic REGEX operations
- In python's `re`, raw python strings are used to allow the usage of `\` as a literal that matches a backslash.
- `re` provides Perl-style regular expression patterns.
- `\d` matches any numeric digit
- `\D` matches any non-numeric digit
- `\w` matches any alphanumeric character [A-Z a-z 0-9 and _]
- `\W` matches any non-alphanumeric character
- `\s` matches any whitespace token (\t \n \r\n )
- `\S` matches any non-whitespace token
- Since `.` is a special token that matches any character except the endline `\n` then you need to skip it `\.` in case you want to match a dot
- `^` and `$` are used to indicate that a regex should occur at the start and/or the end of the sentence
- Using a carat `^` in a optional group like `[0-9]` negates the range.
`[^0-9]` matches any character that isn't in range 0-9.
- `\b` matches any word boundary. A word boundary means: 1) Start of the string. 2) End of the string 3) `\W` "Any non-alphanumeric character"
This character just means that a regex is in a certain boundary but the boundary character isn't matched.
Example: `re.search(r'\ba\b', 'ads a ')` will match the single character `'a'` without its surrounding spaces.
On the other hand, `re.search(r'\Wa\W', 'ads a ')` will also match the spaces ```' a '```.
- On specifying a range don't add a space after the comma!!
`{m,n}` works while `{m, n}` doesn't work.
- `( )` are used to form groups of characters/patterns. This is useful in two cases: 1) Matching a certain string as a whole `(ha){2,}` matches strings like haha, hahaha, .... 2) Capturing certain groups from the regex matching `(bob|alice)` will actually capture the name in some sort of a variable (group) that can be used later.
- Groups are used to parse certain patterns within the string. They are indicated by the `(` and the `)` characters.
For example:
`re.search(r'(\w+):(\w+)', 'Name:Amr')` extracts the field and the value from the line `Name:Amr`
`re.search(r'(\w+):(\w+)', 'Name:Amr').group(1)` will be equal to `Name`
`re.search(r'(\w+):(\w+)', 'Name:Amr').group(2)` will be equal to `Amr`
`group(0)` returns the whole matched string (`Name:Amr` in this case)
- There are some useful flags that are worth using. For example, `re.IGNORECASE` can be used to match both lowercase and uppercase characters `re.match(r'amr', INPUT_STR, re.IGNORECASE)` will match (amr, Amr, aMr, amR, AMr, aMR, AmR, AMR).
- To use multiple flags, these flags are combined using bitwise ORing `|`
- `re.VERBOSE` flag allows the usage of spaces and comments in a regex. According to [python3's regex guide](https://docs.python.org/3/howto/regex.html#compilation-flags): "whitespace within the RE string is ignored, except when the whitespace is in a character class or preceded by an unescaped backslash; this lets you organize and indent the RE more clearly."
Example:
```
charref = re.compile(r"""
&[#]                # Start of a numeric entity reference
(
     0[0-7]+         # Octal form
   | [0-9]+          # Decimal form
   | x[0-9a-fA-F]+   # Hexadecimal form
 )
 ;                   # Trailing semicolon
""", re.VERBOSE)
```
can be used instead of:
```
charref = re.compile("&#(0[0-7]+"
                     "|[0-9]+"
                     "|x[0-9a-fA-F]+);")
```
- Other strings can be used inside the regex, `r'REGEX_START{}REGEX_END'.format(EXTERNAL_STRING)`

## Extensions to the basic operations
- There are some extensions that were added by PERL and ported to python. These Extensions are activated using `?` after a `(`.
- `(?: )` is called a non-capturing group and it's used to match certain patterns but without saving them in variables (groups) to be used later.
- `(?P<GROUP_NAME>GROUP_REGEX)` is used to give a key to a certain group instead of depending on its index.
- Lookaheads are assertions that check that a certain pattern is found (position lookahead) `(?=...)` or not found (negative lookahead) `(?!...)` without actually consuming the characters.
For example, Imagine that we want to match the files with all extensions excluding `.bat`.
The regex `.*[.](?!bat$)[^.]*$` will be composed of:
    - `.*` to match the file name
    - `[.]` to match the dot 
    - Now, we will need to use a negative lookahead. Ensure that the next characters aren't `bat`. The pattern for this is `(?!bat$)` which asserts that the part following the dot isn't `bat$`
    - If the negative lookahead is satisfied, we will match the extension as follows: `[^.]*$` match all characters other than a dot until the end of the string
- Similarly, there are two lookbehind assertions (positive lookbehind) `(?<=...)` and (negative lookbehind) `(?<!...)`

# Things that needs more investigation
- Greedy vs non-greedy matching
- Using Locale aware matching

# Resources and references
- Hackerrank challenges: [https://www.hackerrank.com/domains/regex](https://www.hackerrank.com/domains/regex)