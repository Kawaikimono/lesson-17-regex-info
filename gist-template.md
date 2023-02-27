# Matching an Email with Regex

In this article we will be explaining Regex vaildation for matching an email utilizing the following code: 
`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

## Summary
    The literal translation of the above email regex expression is:
    At the beginning of the string (`^`) please make sure the following group (`()`)  of characters are in this set (`[]`): a-z, 0-9, _, ., and -. Please ensure there are or more (`+`) up to the @. 
    
    After @, group (`()`) this set (`[]`) matching any number between 0-9 (`\d`) or any character in range `a-z`  or one of the following: ., - at least once or more (`+`). Then litterally interpret the dot (`\.`). Finally, in this group (`()`) accept characters from the following set: (`[]`) characters `a-z` and character ".", repeated between 2-6 times `{2,6}` followed by the end of the string `$`.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)

## Regex Components
 
### Anchors
    The following Regex expression has 2 anchors ^ and $.

    The ^ anchor requires that the characters or string of characters that follow it must match in the email while the $ anchor requires that the characters or string infront of it must match in the email.

    An example of this would be ^be
    Meaning the string could start like "be beautiful" or "be handsome" but not "Be someone" since it must match the case.

    The same applies for me&
    "I am me" would work but "You and Me" would not.

### Quantifiers
    Quantifiers {} take in parameters for how many characters you are looking for. There are three diferent ways of putting this:
    1. {4} = I am looking for this instance 4 times exactly
    2. {5,} = I am looking for this instance at least 5 times
    3. {2,6} = I am looking for this instance between 2 to 6 times (as seen in the email verification)

    Additionally, + asks for one of these instances once or more

### Grouping Constructs
    Grouping Constructs are denoted by `()` and are grouped into two different categories: capturing and non-capturing. We are using capturing grouping which basically means something inside of this must be present.

### Bracket Expressions
    Characters in brackets [] are either denoted in ranges or specific characters that must be present. They are case sensitive.

### Character Classes
    Character Classes are set characters or set character groups that have a set meaning.

    . is one of them. Generally it means match any character except `\n` which means new line

    `\d` is one character class present in the email regex. \d means match any Arabic numeral [0-9].

### The OR Operator
    | is the OR Operator. It can be used to say either of these two things are acceptable. 

    ex: (a|b) can equal a or b

### Character Escapes
    \ is an Escape Character. In some instances it has meaning such as the `\d` notation but if the \ character is infront of generally a special character it whipes the meaning of that character. 

    In the email example, \. takes the wild card meaning out of . and turns it into a special character of .

## Author

Aly Geiger coding student. Visit her repo here:  https://github.com/Kawaikimono
