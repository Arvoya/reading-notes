[[102/README|Module 102]]
# Operators & Loops

Reading assignmnet ‘Read08’

## Questions & Answers

1. What is an `expression` in JavaScript? An expression is code that resolves into a value.
2. Why would we use a loop in our code? Create loops can make code repeat itself without having to copy it mulitple times.
3. When does a `for` loop stop executing? A `for` loop stops when the condition is valued to `false`.
4. How many times will a `while` loop execute? `while` loops execute as long as their condition is `true`.

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

Loops are efficient ways to code in an action that repeats itself until a specific parameter stops it. There are multiple ways to create loops; each one tends to work best for a specific situation.

### For Statement

> A `for` loop repeats until a specified condition evaluates to `false`.
#### Example

``` JS
for (let i = 0; i < 10; i++) {
    console.log("i =", i);
}
```

1. `let i = 0` is the initializing expression or `initialization`. The expressions value is `0`, and the new variable that holds it is `i`.
2. `i < 10` is the condition. If the condition is true the loop continues to execute, otherwise the loop would terminate.
3. `i++` is the `afterthought`. If the loop executes, than the value held by `i` will be incremented by `1`. Then it go back to step 2 and repeat until the condition is no longer true.

### While Statement

> A `while` statement executes its statements as long as specified condition evaluates to `true`.

#### Example

``` JS
let x = 0
while (x < 10) {
    console.log("x =", x);
    x++;
}
```

1. `let x = 0` is an expression that values to 0. `x` is the variable that holds this value.
2. `x < 10` is the condition that is tested to be true or false. As the current value of the variable `x` is `0`. This loop will execute.
3. `x++` adds a value of `1` to `x` every time the loop is executed.

#### Avoid Infinte Loops

``` JS
while (true) {
  console.log("Hello, world!");
}
```

1. `true` this will make the loop run indefinitely.