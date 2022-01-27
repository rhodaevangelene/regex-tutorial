# Matching a URL

This tutorial will be breaking down the regular expression ```{ /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ }```, which is used to match URL's in Node.js and MongoDB. 

## Summary

Regular Expressions (or regex) are a string of variables that are used to extract information from textusing specific search patterns. Regex is commonly used to find patterns within a string or to validatestrings of code such as email address's, url's, hex values, HTML tags, and more! In this tutorial we will be going over matching a URL!

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

The regex used to match URL's uses  the ```^``` and ```$``` anchors. The ```^``` siginifies that the string you are searching for is looking for starts with the lower case letter ```h```, and will not capture any string that doesn't start with this letter. The ```$``` means that this is the end of the desired search.

### Quantifiers

The quantifiers required for this expression are ```?```, ```+```, ```{a, b}```, and ```*```. The variable ```?``` is used to match whether or not the string has the character directly in front of it exists. The ```+``` is used to match whether or not there is one or more of the character directly in front of it. The expression ```{a, b}``` is used to set a minimun and maximum floor and ceiling, and affects how many of a certain character is allowed such as: ```Hello{3, 5}``` will not match with ```Hello```, but will match with ```Hellooo```. The variable ```*``` is used to match sequences of numbers, unlike its single variable couterparts ```?``` and ```+```. For example in this regex ```ab(cdefg)```, it will look for either zero or mulitple iterations of ```cdefg```.

### OR Operator

The OR Operator in this regex is ```a[bc]``` and is used to match a string using the variables in stored in the brackets.

### Character Classes

The character classes used in this expression are ```\d```, which matches a single variable that is a number, and ```\.```, which matches any whitespace including tabs and line breaks).

### Grouping and Capturing

This regex has four different groups. The first is ```{(https?:\/\/)}``` and it accepts either a secured or nonsecured webpage url. The second one is ```{([\da-z\.-]+)}``` and it is used to match the ```wwww.```. The third is ```{([a-z\.]{2,6})}``` and it is used to match the webpage name. The final one is ```{([\/\w \.-]*)}``` and it is used to capture the ```{.com}```.

### Bracket Expressions

This expression also uses Bracket Expressions, shown here: ```[a-z\.]```. This allows any character between lowercase ```a``` through lowercase ```z``` match with the URL match expression.

## Author

Written by Rhoda Evangelene

[Github](https://github.com/rhodaevangelene)
