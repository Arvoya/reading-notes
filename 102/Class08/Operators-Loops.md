# Operators & Loops

Reading assignmnet ‘Read08’

## Questions & Answers

1. What is an `expression` in JavaScript?
2. Why would we use a loop in our code?
3. When does a `for` loop stop executing?
4. How many times will a `while` loop execute?

## Notes

Here are the notes I’ve taken while reading the following blogs:

[Expressions & Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) \| [Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#while_statement)

## Expressions & Operators

> An expression is a valid unit of code that resolves to a value.

**Example:**

- `x = 7` \| This expression uses the `=` operator to assign the value seven to the variable `x`. The expression itself evaluates to `7`.

- `1 + 2` \| This expression uses the `+` operator to add `1` and `2` to produce the value `3`. However this expression will be discarded immediately as there is no variable to hold the expression's value.

### Operators

There are different types of JavaScript operators:

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- String Operators
- Logical Operators
- Bitwise Operators
- Ternary Operators
- Type Operators

#### Arithmetic Operators

- \+ Addition
- \- Subtraction
- \* Multiplication
- ** Exponentiation
- \/ Division
- %  Modulus (Division Remainder)
- ++ Increment
- -- Decrement

#### Assignment Operators

| Operator | Example | Same As    |
|----------|---------|------------|
| =        | x = y   | x = y      |
| +=       | x += y  | x = x + y  |
| -=       | x -= y  | x = x - y  |
| *=       | x *= y  | x = x * y  |
| /=       | x /= y  | x = x / y  |
| %=       | x %= y  | x = x % y  |
| **=      | x **= y | x = x ** y |

#### Comparison Operators

- == equal to
- === equal value and equal type
- != not equal
- !== not equal value or not equal type
- \> greater than
- < less than
- \>= greater than or equal to
- <= less than or equal to
- ? ternary operator

## Loops