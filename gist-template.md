# Regex Tutorial - Matching an Email

In this tutorial, I will break down the components of the regular expression for matching an email: <br> **/^([a-z0-9_\\.-]+)@([\da-z\\.-]+)\\.([a-z\\.]{2,6})$/**

## Summary

**/^([a-z0-9_\\.-]+)@([\da-z\\.-]+)\\.([a-z\\.]{2,6})$/** is a regex for matching an email in a search. <br>

>Note: In the markdown of this file, I have added an extra \ before the \\. in the expression so that the backslash will appear in markdown language.  If you were to write >this expression on something other than markdown, there would only be one backslash.

It helps to look at the expression as: <br>
[username] + @ [domain name] + . [com/edu/shop/net(etc)] <br>
I will revisit this in the [conclusion](#conclusion).

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
- [Conclusion](#conclusion)

## Regex Components

Besides the components I'll go over in the following sections, it is important to remember to include the / / in your regex.  Regex are considered literals so if you do not include these slashes, then the search will look for the literal characters you are typing, instead of the search pattern you are providing.

### Anchors

In this example, **/^([a-z0-9_\\.-]+)@([\da-z\\.-]+)\\.([a-z\\.]{2,6})$/**, the '^' and '&#36;' symbols function as anchors. <br>

**^ anchor**: According to the [Full-Stack Blog](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial), "The ^ anchor signifies a string that begins with the characters that follow it."  In our example of finding a matching email, this means that this pattern search will look for strings that begin with **a-z** and **0-9** because those are the characters following the **^** anchor.  The other parts of this first section mean that our search can also include an underscore **_** , a period **.** , and a hyphen **-** . <br>

As you can see in that first section, the period is displayed as a **\\.**  This means the search will look for a literal period/dot.  In regex, the '.' on its own can match any character except for \n 'new line'.  By making it a literal we are escaping this meaning and simply searching for a literal dot, which is a part of every valid email. <br>

**&#36; anchor**: The [Full-Stack Blog](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial) states that the &#36; anchor "signifies a string that ends with the charactrs that precede it." <br>

As you can see, there are parantheses and brackets surrounding the first section, or group, as well as the subsequent groups.  I will cover the role of those in [Grouping ()](#grouping-and-capturing) and [Bracket [] Expressions](#bracket-expressions).

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

In this expression, we have several groups. <br>
**/^([a-z0-9_\\.-]+)@([\da-z\\.-]+)\.([a-z\\.]{2,6})$/** <br>
The groups are created with parentheses () and are:<br>
([a-z0-9_\\.-]+) <br>
([\da-z\\.-]+) <br>
([a-z\\.]{2,6})<br>
Since each of these sections represents the account name, domain name, .com/net/etc, this makes sense.


### Bracket Expressions
Bracket Expressions are also known as a positive character group.  This makes sense because they represent the range of characters we want our search to match ([Full-Stack Blog](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)). <br>

In our example, we have three bracket expressions: <br>
[a-z0-9_\\.-] - we are looking to match letters a through z, numbers 0 through 9, and the string can include a period, underscore, and/or a hyphen<br>
[\da-z\\.-] - \d indicates we are looking for any digit, letters a through z, and the string can include a hyphen<br>
[a-z\\.]


### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

### Conclusion

## Author

Hello! I am currently enrolled in the CWRU Coding Bootcamp (as of July 2024) <br>
Here is my GitHub @ [deepblueseas](https://github.com/deepblueseas)
