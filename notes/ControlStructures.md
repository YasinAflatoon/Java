# Control Structures

Control Structures act like a filter for our programs so we can make sure that the user is on a controlled path.

## Conditions

Sometimes in programs, we have a condition and we need to put the user on two different paths based on that condition.

### if

Use `if` to specify a block of code to be executed, if a specified condition is true.

Format:

``` Java
if (condition) {
  // some code
}
```

Example:

``` Java
if (a > 10) {
    System.out.println(a + 10);
}
```

In this example, if the condition was true('a' were greater than 10), that block of code will be executed (it will be increased by 10.) Else, the program will ignore the block and moves on to the next lines.

### else

Use `else` to specify a block of code to be executed, if the same condition is false.

Example:

``` Java
if (a > 10) {
    System.out.println(a + 10);
} else {
    System.out.println(a - 10);
} 
```

In this example, if the condition was true('a' were greater than 10), that block of code will be executed (it will be increased by 10.) But if the condition was false the second block will be executed only.

#### Ternary Operator

There is also a short-hand if-else, which is known as the ternary operator because it consists of three operands. It can be used to replace multiple lines of code with a single line and is most often used to replace simple if-else statements.

Format:

``` Java
variable = (condition) ? expressionTrue :  expressionFalse;
```

so instead of writing:

``` Java
int hour;
if (hour < 12) {
  System.out.println(hour + "AM.");
} else {
  System.out.println(hour + "PM.");
}
```

you can simply write:

``` Java
int hour;
String result = (hour < 12) ? "AM." : "PM.";
System.out.println(hour + result);
```

### else if

Use `else if` to specify a new condition to test, if the first condition is false.

Example:

``` Java
if (a > 10) {
    System.out.println(a + 10);
} 
else if (a == 10) {
    System.out.println(a);
} 
else System.out.println(a - 10);
```

In this example, if the condition was true('a' were greater than 10), that block of code will be executed (it will be increased by 10.) But if the condition was false the compiler moves to the next condition ('a' is equal to 10), if false, the third block will be executed only.

### switch

Use `switch` to specify many alternative blocks of code to be executed.

Format

``` Java
switch (expression) {
    case x:
        // code block
        break;
    case y:
        // code block
        break;
    default:
        // code block
}
```

* The value of the expression is compared with the values of each `case`.

* When Java reaches a `break` keyword, it breaks out of the switch block. This will stop the execution of more code and case testing inside the block.

* The default keyword specifies some code to run if there is no case match.

## Loops

Loops are among the most basic and powerful programming concepts. A loop in a computer program is an instruction that repeats until a specified condition is reached.

### while

While the condition is true, the block of While statement will be executed.

Format:

``` Java
while (statement){
    // some code
}
```

### do-while

The `do-while` loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.

Format:

``` Java
do {
    // some code
} while (statement)
```

### for

When you know exactly how many times you want to loop through a block of code, use the `for` loop instead of a while loop.

Format:

``` Java
for (statement 1; statement 2; statement 3) {
    // some code
}
```

**statement 1**: is executed (one time) before the execution of the code block.

**statement 2**: defines the condition for executing the code block.

**statement 3**: is executed (every time) after the code block has been executed.

## break

The `break` statement can be also used to jump out of a loop.

Example:

``` Java
for (int i = 0; i < 5; i++) {
  if (i == 4) {
    break;
    System.out.println(i);
  }
}
```

The output will be:

``` Batch
0
1
2
3
```

* break command actually ignores the rest of the code block.

## continue

The continue statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

``` Java
for (int i = 0; i < 6; i++) {
  if (i == 4) {
    break;
    System.out.println(i);
  }
}
```

the output will be

``` Batch
0
1
2
3
5
```
