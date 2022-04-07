# Operators

Java provides a rich set of operators to manipulate variables. We can divide all the Java operators into the following groups

* Arithmetic Operators
* Relational Operators
* Logical Operators
* Assignment Operators
* Bitwise Operators
* Misc Operators

In this tutorial we just focus on first four operators.

## Basic Operators

In this tutorial we just focus on first four operators.

### The Arithmetic Operators

Arithmetic operators are used in mathematical expressions in the same way that they are used in algebra. The following table lists the arithmetic operators.

| Operator           | Discription                                                            |
| ------------------ | ---------------------------------------------------------------------- |
| + (Addition)       | Adds values on either side of the operator.                            |
| - (Subtraction)    | Subtracts right-hand operand from left-hand operand.                   |
| * (Multiplication) | Multiplies values on either side of the operator.                      |
| / (Division)       | Divides left-hand operand by right-hand operand.                       |
| % (Modulus)        | Divides left-hand operand by right-hand operand and returns remainder. |
| ++ (Increment)     | Increases the value of operand by 1.                                   |
| -- (Decrement)     | Decreases the value of operand by 1.                                   |

So let's try them in our IDE.

![ArithmeticResult](/media/img06.png)

About Increment and Decrement operators, there is two way to use them: Left-side of variable and right-side. If you use them in right-side, it would work in our code with it's initial value in each line, then it will icreases(decreases) by 1. But it left-side case, icreament(decreamet) happens first, then it then the variable enrolls in program.

![De/Increament](/media/img07.png)

### The Relational Operators

Relational operators test or define some kind of relation between two entities. The following table lists the relational operators.

| Operator                 | Discription                                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| == (Equal to)            | Checks if the values of two operands are equal or not, if yes then condition becomes true.                                      |
| != (Not equal to)        | Checks if the values of two operands are equal or not, if no then condition becomes true.                                       |
| > (Greater than)         | Checks if the value of left operand is greater than the value of right operand, if yes then condition becomes true.             |
| < (Less than)            | Checks if the value of left operand is less than the value of right operand, if yes then condition becomes true.                |
| >= (Greater or equal to) | Checks if the value of left operand is greater than or equal to the value of right operand, if yes then condition becomes true. |
| <= (Less or equal to)    | Checks if the value of left operand is less than or equal to the value of right operand, if yes then condition becomes true.    |

![RelationalResult](/media/img08.png)

### The Assignment Operators

Assignment operators are used in Java to assign values to variables.

| Operator | Discription                                                                                                                    |
| ---------| ------------------------------------------------------------------------------------------------------------------------------ |
| =        | **Simple assignment operator.** Assigns values from right side operands to left side operand.                                  |
| +=       | **Add AND assignment operator.** It adds right operand to the left operand and assign the result to left operand.              |
| -=       | **Subtract AND assignment operator.** It subtracts right operand from the left operand and assign the result to left operand.  |
| *=       | **Multiply AND assignment operator.** It multiplies right operand with the left operand and assign the result to left operand. |
| /=       | **Divide AND assignment operator.** It divides left operand with the right operand and assign the result to left operand.      |
| %=       | **Modulus AND assignment operator.** It takes modulus using two operands and assign the result to left operand.                |

Unlike math we have two seperate oprators for assignment and equality Remember avoid confliction between assignment operator (=) and equality operator (==).

![AssignmentResult](/media/img09.png)

### The Logical Operators

Logical operators are used to check whether an expression is true or false.

| Operator     | Discription                                                                                                                                       |
| ----------   | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| &&           | Called Logical AND operator. If both the operands are non-False, then the condition becomes true.                                                 |
| \|\|         | Called Logical OR Operator. If any of the two operands are non-False, then the condition becomes true.                                            |
| !            | Called Logical NOT Operator. Use to reverses the logical state of its operand. If a condition is true then Logical NOT operator will make false.  |

![LogicalResult](/media/img10.png)

In this tutorial we're gonna skip bitwise operators but if you are intersted you can check [Geek For Geeks](https://www.geeksforgeeks.org/bitwise-operators-in-java/) for bitwise operators.

## Operators Precedence

Operator precedence determines the order in which the operators in an expression are evaluated. The closer to the top of the table an operator appears, the higher its precedence.

| Operators            | Precedence                                                      |
| -------------------- | --------------------------------------------------------------- |
| postfix              | `expr++` `expr--`                                               |
| prefix and unary     | `++expr` `--expr` `+expr` `-expr` `~` `!`                       |
| multiplicative       | `*` `/` `%`                                                     |
| additive             | `+` `-`                                                         |
| shift                | `<<` `>>` `>>>`                                                 |
| relational           | `<` `>` `<=` `>=` `instanceof`                                  |
| equality             | `==` `!=`                                                       |
| bitwise AND          | `&`                                                             |
| bitwise exclusive OR | `^`                                                             |
| bitwise inclusive OR | `\|`                                                            |
| logical AND          | `\|\|`                                                          |
| ternary              | `? :`                                                           |
| assignment           | `=` `+=` `-=` `*=` `/=` `%=` `&=` `^=` `\|=` `<<=` `>>=` `>>>=` |
