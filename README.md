# Regex Tutorial
the purpose of this module was to explain how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.
link: https://maximus-cristian.github.io/regex-tutorial/
gist:Regex Tutorial: Matching a Hex Value
Regex, or regular expressions, are sequences of characters that specify a search pattern in text. Regular expressions are strings of text that allow you to create patterns that can assist in matching, locating, and managing text.

Summary
I will be discussing the specific regex for mataching a hex value. Regexes can be used to validate a hexidecimal color code, which are values that tell the display how much of a color to show. In the description below, I will cover the many aspects of regexes and specifically the expression for matching a hex value.

Matching a Hex Value – /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Table of Contents
Anchors
Quantifiers
Grouping Constructs
Bracket Expressions
Character Classes
The OR Operator
Flags
Character Escapes
Regex Components
Anchors
Anchors are used to declare an aspect of the string, but when they stand alone they are not considered regular expressions. For example, in the snippet of code above, the character ^ is an anchor and it is used to state the beginning of the following expression. On the other end of the expression, $ is also considered an anchor but its purpose is quite the opposite; in this case $ refers to the end of the regex.

Quantifiers
Quanitifiers are used to represent how often a specific character must be found in order to classify as a match. The ? in the regex above implies a value of 0 or 1; the $ is followed by the character # meaning it is optional in that instance. For example, the regex above contains {6} which implies that this quantifier will expect 6 characters in the string containing characters between a-f or integers between 0-9.

Grouping Constructs
This is one of the more straight forward concepts of regexes; the () is used to group the entire expression together. Rather than each character standing alone, utilizing the () ensures that the expression is seen as one, and cannot be picked apart. The characters found outside the (), are used as paramters to mark the beginning and the end of the regex.

Bracket Expressions
Similar to how the () are utilized, bracket expressions are used to group a specific pattern of characters. As seen in our code snippet, hyphens are used to signify a range. For example, a-f is meant to distinguish any characters between those two letters. Whereas 0-9 is used to indicate any number between that parameter. When these two paramters are grouped within aa single bracket expression, our regex is looking to match only characters that follow the set of rules placed within this brackets. Also, how we see three different sets of hard brackets, those are three completely unrelated set of rules in which our hex values may match.

Character Classes
Characters classes work to define a range of characters that are meant to match the hex value. In this case, 0-9 includes any numbers that fall specifically into that range. This concept works similarly with letters, where in the snippet above a-f stands for any characters that fall inbetween that set parameter.

The OR Operator
The OR operator is used between expressions to signify a match that may happen in one set, OR another. The character | is used to seperate an expression with another, and works to look for values that match either side of the |. In our case, we have [a-f0-9]{6}|[a-f0-9]{3}, where on the left of | is one set of rules a match may be classified by, and on the right is a different set of values in which a match may be classified.

Flags
Flags (i, g, s, m, u) are optional parameters to a regex that modifies its behavior of searching. Although our snippet does not contain flags, a fleg is classified using a single lowercase alphabetic letter and each flag has its own meaning and purpose.

Character Escapes
Character escapes such as a backslash, /, are used to escape certain letters that represent common character classes.
