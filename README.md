# Regex Tutorial Starter Code
Summary
This is a tutorial on how Regex is used to match a Hex Value . They are regularly used to validate input. /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ is the syntax that I will be using.

Hex Code is always in a 6-digit alphanumeric sequence. Hexadecimal color codes are used to tell the computers the intensity of a colors red, green and blue components, each represented by eight bits. The regex string will return a # Number sign character followed by either a 6 or 3 character length code with only lowercase letters a,b,c,d,e,or f or numbers 0,1,2,3,4,5,6,7,8, or 9.

Table of Contents
Anchors
Quantifiers
OR Operator
Character Classes
Flags
Grouping and Capturing
Greedy and Lazy Match
Boundaries
Regex Components
Anchors
The starting ^ caret and ending $ dollar sign are both anchors in the example string. /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ If you have a string consisting of multiple lines, like first line\nsecond line (where \n indicates a line break), it is often desirable to work with lines, rather than the entire string. Therefore, most regex engines discussed in this tutorial have the option to expand the meaning of both anchors. ^ can then match at the start of the string (before the f in the above string), as well as after each line break (between \n and s). Likewise, $ still matches at the end of the string (after the last e), and also before every line break (between e and \n).

Quantifiers

Quantifiers indicate numbers of characters or expressions to match. The quantifier for our example is the section in the curly braces.

? - matches the pattern zero or one time {} - curly brackets mean that the pattern matches exactly n number of times. In this case, 6 or 3 times.

Exact count {n} A number in curly braces {n}is the simplest quantifier. When you append it to a character or character class, it specifies how many characters or character classes you want to match. For example, the regular expression /\d{4}/ matches a four-digit number. It is the same as /\d\d\d\d/:

The range {n,m} The range matches a character or character class from n to m times.

For example, to find numbers that have two, three or four digits, you use the regular expression /\d{2,4}/g

OR Operator

The example syntax uses an OR operator known as | Vertical line or pipe. There is a | Pipe between two characters classes. This creates 2 alternative groups. This allows the search to find and match either group.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
The first alternative is before the | pipe [a-f0-9] will return 6 characters.

The second alternative after the | Pipe will return 3 characters.

Character Classes


Character classes are found betwen [...] square brackets. They are used to create a list of allowable characters. In the example syntax there are two character classes. They look exactly the same because they are, however the quantifier is what makes each class return a different number of characters.

The example uses [a-f0-9]

a-f = This is the range that matches a case sensitive single character of: a,b,c,d,e, or f.
0-9 = This is the range that matches a case sensitive single digit of: 0,1,2,3,4,5,6,7,8, or 9

Flags

Expression flags change how the expression is interpreted. Flags follow the closing forward slash of the expression.

i Ignores case
g Global search retain the index of the last match, allowing subsequent searches to start from the end of the previous match. Without the global flag, subsequent searches will return the same match.
m Multiline flag When the multiline flag is enabled, beginning and end anchors (^ and $) will match the start and end of a line, instead of the start and end of the whole string.
u Unicode
y The expression will only match from its lastIndex position and ignores the global (g) flag if set. Because each search in RegExr is discrete, this flag has no further impact on the displayed results.
s Dot (.) will match any character, including newline.

Grouping and Capturing

Anything found inside of ( round brackets ) creates a capture group. Everything inside that (...) is treated as a single unit. So with the example syntax /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ there is one capture group with two characters sets seperated by an OR Operator.

Greedy and Lazy Match

Remember the ? quantifier we talked about earlier? The single ? by defult is considered greedy. This means it will match as many occurrences of the given pattern as possible. A lazy match would be denoted as a double ??. Lazy means as few occurrences of the pattern as possible, however our example syntax is considered greedy not lazy.

Boundaries

Boundries used are the ^caret to siginify the start of the string and the $ dollar sign signifies the end of the string.

Author

I am Rhoda, A Student of the University of Toronto Coding Bootcamp. https://github.com/rhodaevangelene
