# Welcome to VSCOWorld!

VSCOgirl is a programming language developed by Sara Ann as part of the Honors Programming Languages curriculum in the Spring of 2020.

This language was developed according to the processes set forth by [Dr. John C. Lusth](https://eng.ua.edu/people/dr-john-lusth/), Associate professor in the Department of Computer Science, University of Alabama, Tuscaloosa, AL.

# Becoming a VSCOgirl

## Table of Contents

1. [Hello, World!](#hello-world)
2. [Notation](#notation)
1. [Defining Variables and Functions](#defining-variables)
1. [Calling Functions](#calling-functions)
2. [Writing Conditional Statements](#writing-conditional-statements)
1. [Index of Special Characters](#special-characters)


## Hello, world!

The following program prints `"Hello, world!"` to the console:

```
@POST ["Hello, world"]
```

`POST` is a built-in that works like `println` in many other languages.

## Notation
VSCOgirl uses *prefix notation* which means that operators go before arguments. Expressions are notated with brackets to indicate the arguments they contain.

For example, adding 5 and 6 would look like this:
```
+ [5 6]
```
If you wanted to nest addition statements, the notation for that would be:
```
+ [ (+ [5 6] ) (+ [3 4 5]) ]
```
### Comments
Commenting is done using `:`
A commented out line would look like this:
```
: helpful information about your code :
```

## Defining Variables and Functions

Variables and functions are declared using `#` 
They can be declared without being initialized:
```
#C1~
```
Or instantiated in a single line:
```
#C1 (5) 
```
```
#C1 [x] (*[5 6]) 
```
*Variables and functions are treated exactly the same in my language, but brackets and parentheses are used to differentiate between parameters and definitions. Parameters are always in square brackets, while function definitions are in parentheses*

## Naming Variables and Functions
In the spirit of VSCO filters, functions and variables are usually named using a pair of letters and numbers A-ZZ and 0-99.
For example, a function or variable could be named F12 or AB1. This is not a requirement, because VSCOgirl supports variables and functions being named any alphanumeric phrase. This is possible because VSCOgirl doesn't have keywords beyond a couple built in functions.

## Calling Functions

Function calls use the `@` symbol. 
An example function call using the parameters x and y:
```
@U8 [x y]
```
### Implicit Returns

Returns are implicit in VSCOgirl, so the final valuee or final expression evaluated at the end of the block of code is returned.

## Writing Conditional Statements
VSCOgirl supports two types of conditional statements: 
1. `if` statements, which use `$`
2. `while` loops, which use `&`
### Booleans
In VSCOgirl, booleans look a little different than in Java.
`^` represents `true`, while `^^` represents `false`
### If Statements
An example `if` statement would look like this:
```
$[= x y] { @POST ["This condition was met! Time to celebrate!"] }
```
### While Loops
An example `while` loop would look like this:
```
&[= x y] { #F2 (^^) }
```
## Special Characters

| Symbol | Functionality |
| :---: | --- |
| `#` | Function or variable declaration |
| `~` | Marks the end of a declaration |
| `@` | Function call |
| `[ ]` | Contains a parameter list `[parameter parameter parameter ...]` |
| `( )` | Contains definitions / expressions `(* [x x] )` or `(+ [2 4] )`|
| `{ }` | Contains the block of statements that execute with an `if` statement or `while` loop | 
| `$` |  `if` statement |
| `&` |  `while` loop |
| `{ }` | Contains blocks of code / statements to be evaluated, used with `&` (`while`) loops |
| `: :` | Comments out enclosed statement |
