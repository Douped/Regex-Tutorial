# Regex Tutorial

Welcome to my Regex Tutorial! In this tutorial, I will explore various components of regular expressions (regex) and provide detailed explanations for each component. Regular expressions are powerful patterns used to match and manipulate text. Understanding regex can greatly enhance your text processing and search capabilities.

## Summary

In this tutorial, we will cover the following regex concepts:

**Anchors**: Anchors specify the position of a pattern in the text.

**Quantifiers**: Quantifiers define the number of occurrences of a pattern.

**OR Operator**: The OR operator allows for matching alternative patterns.

**Character Classes**: Character classes define sets of characters to match.

**Flags**: Flags modify the behavior of the regex matching process.

**Grouping and Capturing**: Grouping and capturing enable the extraction of specific parts of a match.

**Bracket Expressions**: Bracket expressions define custom character ranges.

**Greedy and Lazy Match**: Greedy and lazy quantifiers control the greediness of pattern matching.

**Boundaries**: Boundaries define specific positions in the text.

**Back-references**: Back-references match previously captured groups.

**Look-ahead and Look-behind**: Look-ahead and look-behind assertions enable conditional matching.

Each section will provide a detailed explanation of the corresponding regex component and its usage.

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

## Anchors

Anchors are regex components that specify the position of a pattern in the text. There are two types of anchors:

- The caret (`^`) anchor matches the beginning of a line.
- The dollar sign (`$`) anchor matches the end of a line.

For example, the regex `^Hello` matches the word "Hello" only if it appears at the beginning of a line, while the regex `world$` matches the word "world" only if it appears at the end of a line.

Anchors are useful for validating or extracting specific patterns that must occur at the beginning or end of a line.

## Quantifiers

Quantifiers are regex components that define the number of occurrences of a pattern. They allow you to specify the quantity or range of repetition for a particular pattern. Some common quantifiers include:

- The asterisk (`*`) quantifier matches zero or more occurrences of the preceding pattern.
- The plus (`+`) quantifier matches one or more occurrences of the preceding pattern.
- The question mark (`?`) quantifier matches zero or one occurrence of the preceding pattern.
- The curly braces (`{}`) quantifiers allow you to specify an exact quantity or a range of occurrences.

For example, the regex `a+` matches one or more occurrences of the letter "a", while the regex `ab{2,4}` matches "abb", "abbb", or "abbbb".

Quantifiers provide flexibility in matching patterns with varying repetition.

## OR Operator

The OR operator (`|`) allows for matching alternative patterns. It enables you to specify multiple patterns, and if any of them match, the overall regex will be considered a match.

For example, the regex `cat|dog` matches either "cat" or "dog". If either of these words appears in the text, the regex will successfully match.

The OR operator is useful when you want to match different alternatives at a specific position in the text.

## Character Classes

Character classes define sets of characters to match. They allow you to specify a range or a list of characters that the regex should match.

Some common character class expressions include:

- `[abc]`: Matches any single character that is either "a", "b", or "c".
- `[0-9]`: Matches any single digit.
- `[A-Z]`: Matches any single uppercase letter.
- `[^a-z]`: Matches any single character that is not a lowercase letter.

Character classes provide a convenient way to match specific groups of characters within a larger pattern.

## Flags

Flags modify the behavior of the regex matching process. They are appended to the end of the regex and can change how the regex engine interprets the pattern.

Some common flags include:

- `i` (case-insensitive): Matches characters regardless of case.
- `g` (global): Matches all occurrences of a pattern, not just the first one.
- `m` (multiline): Allows anchors (`^` and `$`) to match the beginning and end of lines within a multi-line string.

For example, the regex `/hello/gi` will match "hello", "Hello", "HELLO", and any other case variation of "hello" in a global manner.

Flags provide additional control and flexibility in the regex matching process.

## Grouping and Capturing

Grouping and capturing enable the extraction of specific parts of a match. They allow you to enclose parts of a regex pattern within parentheses, creating capture groups.

For example, the regex `(\d{3})-(\d{3})-(\d{4})` matches a phone number in the format "###-###-####". The three sets of parentheses create three capture groups, each capturing a specific part of the phone number.

Capture groups are useful for extracting and manipulating specific portions of a matched pattern.

## Bracket Expressions

Bracket expressions define custom character ranges. They allow you to specify a set of characters to match, including ranges of characters.

For example, the regex `[aeiou]` matches any single vowel character, while the regex `[0-9]` matches any single digit.

Bracket expressions provide a way to define specific character ranges within a regex pattern.

## Greedy and Lazy Match
# Greedy Match:

By default, quantifiers in regular expressions are greedy. A greedy quantifier tries to match as much of the input text as possible while still allowing the overall pattern to match. It will match as many occurrences of the preceding pattern as it can.

For example, consider the regex pattern a+ applied to the input string aaa. The greedy match will result in a single match that includes all three "a" characters (aaa), as it tries to match as much as possible.

Greedy quantifiers are denoted with + (one or more), * (zero or more), ? (zero or one), or {m,n} (between m and n occurrences).

# Lazy Match (also known as Non-greedy or Reluctant Match):

In contrast, a lazy quantifier (also known as non-greedy or reluctant quantifier) matches as little of the input text as possible while still allowing the overall pattern to match. It will match the fewest occurrences of the preceding pattern.

To make a quantifier lazy, you can append a ? after it.

For example, using the pattern a+? on the input string aaa, the lazy match will result in three separate matches, each matching a single "a" character (a, a, a).

Lazy quantifiers are useful when you want to find the shortest possible match or when you want to match text in a specific context.
