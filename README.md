# Email-Regex-Explained

## Match an Email using Regex

This tutorial will explain how regex is used to match emails using the expression ```md /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```. This is useful when you want to post a form request with a valid email inside. This is especially useful when using technologies like Inquirer and MongoDB.

## Summary

A regular expression is a array of characters that defines a search pattern. Regular expressions are commonly used to find/replace characters in a string, or validate an input. This tutorial will explain the components and functionality of a regex.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

# Regex Components

### Anchors

The anchors in this Regex expression are ```^```, ```$``` and ```(m)```. The ```^``` anchor indicates the begining and end of a string unless ```(m)``` is used, indicating multiline.

### Quantifiers

The quantifiers in this regex statement include ```+```, ```{2,6}```, and ```[a-z\.]```. The ```+``` operator connects the users email name, with an email service and a domain (like ```.com```). The quantifier ```{2,6}``` which allows for a range of 2 to 6 characters in the character set ```[a-z\.]```.

## Character Classes
The character class in this expression is ```\d``` which matches a single character containing the digits 0-9. Since it only matches a single character, it will only match a single digit such as '3' but not '33'.

## Grouping and Capturing

There are three catchign groups in this expression, the first is ```([a-z0-9_\.-]+)```, the second is ```([\da-z\.-]+)```, and the third is ```([a-z\.]{2,6})```. The first catching group, ```([a-z0-9_\.-]+)``` captures the characters in the users email before the @ sign. The second group, ```([\da-z\.-]+)``` is used to capture the email provider, or the bit between ```@``` and ```.``` in the email address. The third is ```([a-z\.]{2,6})``` and simply captures the domain name (such as ```.com``` or ```.net```)

## Bracket Expressions

bracketed expressions are used to validate a set of characters in a partial string. In this scenerio, the bracketed expression ```[a-z0-9_\.-]``` matches any letter a-z case sensitive, and any character 0-9 aswell as "_","-", and ".". ```[\da-z\.-]``` is a bracketed expression that matches a single digit 0-9 and any character a-z case sensitivly. Finally ```[a-z\.]``` matches characters 0-9, a-z case sensitive, and the "." character.

## Greedy and Lazy Match

The regex includes greedy matches since it uses the "+" quantifier. This means, it will match as many times as possible giving back as needed. Another greedy quantifier in this regex is ```{}``` when matching ```{2,6}``` in the third capture group.



### Take a look at my other projects at this link!
[my Github](https://github.com/BihonAnon)