# Operators

Java provides a rich set of operators to manipulate variables. We can divide all the Java operators into the following groups

* Arithmetic Operators
* Relational Operators
* Logical Operators
* Assignment Operators
* Bitwise Operators
* Misc Operators

## Basic Operators

In this tutorial, we just focus on the first four operators.

### The Arithmetic Operators

Arithmetic operators are used in mathematical expressions in the same way that they are used in algebra. The following table lists the arithmetic operators.

| Operator           | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- |
| + (Addition)       | Adds values on either side of the operator.                            |
| - (Subtraction)    | Subtracts the right-hand operand from the left-hand operand.                   |
| * (Multiplication) | Multiplies values on either side of the operator.                      |
| / (Division)       | Divides left-hand operand by right-hand operand.                       |
| % (Modulus)        | Divides left-hand operand by right-hand operand and returns the remainder. |
| ++ (Increment)     | Increases the value of operand by 1.                                   |
| -- (Decrement)     | Decreases the value of operand by 1.                                   |

So let's try them in our IDE.

![ArithmeticResult](/media/img06.png)

About Increment and Decrement operators, there is two way to use them: Left-side of the variable and the right side. If you use them on the right-side, it would work in our code with its initial value in each line, then it will increase(decrease) by 1. But in the left-side case, increment(decrement) happens first, then the variable enrolls in the program.

![De/Increament](/media/img07.png)

### The Relational Operators

Relational operators test or define some kind of relation between two entities. The following table lists the relational operators.

| Operator                 | Description                                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| == (Equal to)            | Checks if the values of two operands are equal or not, if yes then the condition becomes true.                                      |
| != (Not equal to)        | Checks if the values of two operands are equal or not, if no then the condition becomes true.                                       |
| > (Greater than)         | Checks if the value of the left operand is greater than the value of the right operand, if yes then the condition becomes true.             |
| < (Less than)            | Checks if the value of the left operand is less than the value of the right operand, if yes then the condition becomes true.                |
| >= (Greater or equal to) | Checks if the value of the left operand is greater than or equal to the value of the right operand, if yes then the condition becomes true. |
| <= (Less or equal to)    | Checks if the value of the left operand is less than or equal to the value of the right operand, if yes then the condition becomes true.    |

![RelationalResult](/media/img08.png)

### The Assignment Operators

Assignment operators are used in Java to assign values to variables.

| Operator | Description                                                                                                                    |
| ---------| ------------------------------------------------------------------------------------------------------------------------------ |
| =        | **Simple assignment operator.** Assigns values from right side operands to left side operands.                                  |
| +=       | **Add AND assignment operator.** It adds the right operand to the left operand and assigns the result to the left operand.              |
| -=       | **Subtract AND assignment operator.** It subtracts the right operand from the left operand and assigns the result to the left operand.  |
| *=       | **Multiply AND assignment operator.** It multiplies the right operand with the left operand and assigns the result to the left operand. |
| /=       | **Divide AND assignment operator.** It divides the left operand with the right operand and assigns the result to the left operand.      |
| %=       | **Modulus AND assignment operator.** It takes modulus using two operands and assigns the result to the left operand.                |

Unlike math we have two separate operators for assignment and equality Remember to avoid conflict between assignment operator (=) and equality operator (==).

![AssignmentResult](/media/img09.png)

### The Logical Operators

Logical operators are used to checking if an expression is true or false.

| Operator     | Description                                                                                                                                       |
| ----------   | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| &&           | Called Logical AND operator. If both the operands are non-False, then the condition becomes true.                                                 |
| \|\|         | Called Logical OR Operator. If any of the two operands are non-False, then the condition becomes true.                                            |
| !            | Called Logical NOT Operator. Use to reverse the logical state of its operand. If a condition is true then the Logical NOT operator will make false.  |

![LogicalResult](/media/img10.png)

In this tutorial, we're gonna skip bitwise operators but if you are interested you can check [Geek For Geeks](https://www.geeksforgeeks.org/bitwise-operators-in-java/) for bitwise operators.

## Operators' Precedence

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
