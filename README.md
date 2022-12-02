# regex_tutorial: How to use Regex for URL validation

## Summary 

In this tutorial we will explain how to match a URL with regex. 

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## Table of Content

* Anchors
* Quantifiers
* Character Classes
* Grouping and Capturing
* Bracket Expressions

## Regex Compnents

### Ancors

* Anchors tell the regular expressions where to start and end in the search. This character `^` is used to match an expression to its right at the start of a string. The `$` is used to match an expretion to its left at the end of a string. When both `^` & `$` are existing together, it indicates that the string must match whatever is in between them. In the expression provises, the entire collection of characters is weappped in both `^` + `$` making the search exact.

### Quantifiers

* Quantisiers determine how many instances os a charater, group, or charater class can be present in the expression. This cominarrtion of characters has a few quantifiers. See the table od contents for more information on Groups, Capturing and Brackets.

* This `*` charater specifies an expression to its left for zero or more. the third capture group: `([\/\w\.-]*)*`, searches for any instance of the criteria within the brackets, then as many instances of that criteria afterwards, including the possibility of no matches.

* the `+` charater specifies an expression to its left for one or more times (but not zero). in the capture group: `([\da-z\.-]+)`, the `+` till match any number of instances based off of the declaration in square brackets.

* the `?` character specifies an expression to its left for zero or one times. In the first capture group `(https?:\/\/)?` will accept zero or one instance of "s".

* The {} characters are used to match a particular number of occurrences defined in the curly bracket for the string to its left. {2,6} within the last capture group: `([a-z\.]{2,6})` searches for 2 to 6 instances of a character based off the criteria within the square brackets.

## character classes

* A character class defines a set of character that can occur within the string.

* `\d` is used to match one decimal digit, which means from 0 to 9.

* `\w` is used to match the alphanumeric [0-9a-zA-Z] characters.

* `\/` is used to match a single character of `/`.

* `\.` is used to match a single character of `.`.

## Grouping and capturing 

* A caputre group treats everything within the parentheses as a single unit.

* There are 4 instances of capure sroups within the url regex expression.

1. `^(https?:\/\/)?`

2. `([\da-z\.-]+)\.`

3. `([a-z\.]{2,6})`

4. `([\/\w \.-]*)*`

## Bracket Expressions

* Bracket Expressions can handle many "or" situations.

* In the above capture groups, group 2 would allow the search of a string with any of the possible characters within it, wherther it be a-z or 0-9

## Helpfull Links

When reserching regex I found (link to regex101)[https://regex101.com/library?orderBy=MOST_POINTS&search=], this sight is a great tool for real time regex use and any regex troubleshooting.