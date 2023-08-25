ja REgex tutorial
# REgex tutorial

A regular expression, often abbreviated as REGEX, is a tool used to identify specific patterns or sequences in a string. 
For instance, a commonly used REGEX pattern is designed to validate the typical structure of an email address.

## Summary

The regular expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ is crafted to validate the format of an email address. In this pattern, each segment ensures that the email conforms to a standard structure: it starts with specific characters, is followed by the '@' symbol, and concludes with the domain. Properly employing this regex helps in ensuring that users input email addresses adhering to the accepted norms.
Additionally, such validations enhance the integrity of data collected and reduce potential errors.
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
In Regex, the ^ symbol denotes the start of a string, while the $ symbol signifies its end. Within our provided regular expression, these anchors help specify the exact positioning of a pattern. 
Using these anchors enhances the precision of the pattern match, ensuring it aligns perfectly with the desired string boundaries.

### Quantifiers
In the provided regular expression, we observe specific quantifiers: the + sign matches one or more instances of the previous element, and {2,6} ensures that the preceding item appears between 2 to 6 times. For instance, {2,6} would match sequences having exactly 2 digits, while {2,4} is geared to recognize sequences of 2 or more characters, up to 4. These quantifiers give us flexibility in dictating how many times 
a particular pattern should appear for a successful match, enhancing the adaptability of our regex criteria.

### OR Operator

In regex, the OR operation is signified by the vertical bar "|". It lets you match the pattern before or after this symbol.
### Character Classes
Character Classes in regex help in identifying particular types of characters from a predefined group. 
In the regular expression we're discussing, two character classes are evident: . and \d. The symbol . 
typically matches any character excluding a newline. When we prepend a dot with a backslash, like \. 
it then represents the actual dot character, rather than its usual wildcard meaning. Meanwhile, \d is used to match any 
individual digit and is synonymous with [0-9].

To illustrate, in the pattern a\.c, it will find matches for the literal string "a.c". In this context, 
the dot is interpreted just as a period and not as a wildcard character.

### Flags
In the given regular expression, the g flag is present, signifying a global search. This means the regex will seek out all matches in a string, rather than stopping at the first one. By using the global flag, we ensure comprehensive scanning of the entire text, 
capturing every instance that matches the specified pattern.

### Grouping and Capturing
The provided example features a grouping: ([a-z0-9_.-]+). Within this group, the + indicates a match for one or more of the characters specified inside the square brackets [a-z0-9_.-]. Here, a-z covers lowercase letters from 'a' to 'z', 0-9 encompasses numbers from '0' to '9', _ represents the underscore, . denotes the period, and - stands for the hyphen. By organizing these elements into a group, the regex can treat them as a single unit, 
allowing for more complex pattern matching strategies.

### Bracket Expressions

Bracket expressions, enclosed by square brackets [], define a set of characters for matching purposes.
In our provided regex, there are three distinct bracket expressions: ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}).

To illustrate how bracket expressions work, consider the pattern [abc]. This will match any single character from the set, which means it could be 'a', 'b', or 'c
### Greedy and Lazy Match
In the provided email-matching code, neither greedy nor lazy quantifiers are explicitly used. Utilizing such quantifiers can influence how the regex engine captures matches, potentially optimizing the pattern for specific use cases.

### Boundaries
The metacharacter \b functions as an anchor, similar to the caret (^) and the dollar sign ($). It identifies a position known as a "word boundary" without consuming any characters, meaning its match has a length of zero. Recognizing these word boundaries is 
essential when we aim to match entire words without mistakenly capturing adjacent characters.

### Back-references

In regex, back-references provide a way to reference previously captured groups within the same pattern. They're indicated by a backslash and a numeral, with the numeral pointing to the sequence of the captured group, such as \1 for the first group and \2 for the second. 
This feature is handy for identifying repetitive sequences or for modifying matches based on the original captured content.
### Look-ahead and Look-behind
"Lookaround" encompasses both lookahead and lookbehind and, like the start/end of line or word anchors, these are zero-length assertions. While they initially match characters, they don't consume them; instead, they only indicate if a match is possible. Hence, they're termed "assertions". 
They enhance regex by making certain pattern matches feasible or simplifying complex ones.

## Author
Neeraja Narayanan

A coding passionate
https://github.com/hineeraja