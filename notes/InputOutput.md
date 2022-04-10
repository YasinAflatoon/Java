# Input and Output

In programming, we always need to have interaction with users to show to or get data from them. Data that the user enters will be processed by algorithms and formulas we write in our code and finally, an appropriate result should be shown to the user. So our program should support features to meet this need.

## Input

The `Scanner` class is used to get user input, and it is found in java.util package.

To use the Scanner class, create an object of the class and use any of the available methods found in the Scanner class documentation.

In the heading of your code type this:

``` Java
import java.util.Scanner;
```

then type the following code in main method:

``` Java
Scanner keyboardInput = new Scanner(System.in);
```

![Scanner](/media/img11.png)

The first word (Scanner) is for calling the class and we name it "keyboradInput" in the second word. After the equal sign, we create a Scanner object and we tell the System that we need to receive an input.

after creating scanner we need to know which type of data (variable) we're gonna receive to store it in an appropriate variable. Scanner must use a method to specify the input format:  

### Input Types

| Method          | Description                             |
| --------------- | --------------------------------------- |
| `nextBoolean()` | Reads a **boolean** value from the user |
| `nextByte()`    | Reads a **byte** value from the user    |
| `nextshort()`   | Reads a **short** value from the user   |
| `nextInt()`     | Reads an **int** value from the user    |
| `nextLong()`    | Reads a **long** value from the user    |
| `nextDouble()`  | Reads a **double** value from the user  |
| `nextFloat()`   | Reads a **float** value from the user   |
| `nextline()`    | Reads an **String** value from the user |

and we use this method like the following:

``` Java
boolean isMarried = keyboeadInput.nextBoolean();
byte age = keyboeadInput.nextByte();
short height = keyboeadInput.nextshort();
int id = keyboeadInput.nextInt();
long phoneNumber = keyboeadInput.nextLong();
double score = keyboeadInput.nextDouble();
float bmi = keyboeadInput.nextFloat();
String description = keyboeadInput.nextline();
```

> There is no "nextChar()" method for reading a char value, to do that you need to write the following code:

``` Java
char grade = keyboardInput.next().chatAt(0);
```

> next() function returns the next token/word in the input as a string and charAt(0) function returns the first character in that string.

## Output

As mentioned before we use `System.out.println()` to show an output but we're gonna add some points here:

* There are two more methods to replace with println(): print() and printf().

> print(): It prints string inside the quotes.</br>println(): It prints string inside the quotes similar like print(): method. Then the cursor moves to the beginning of the next line.</br>printf(): It provides string formatting (similar to printf in C/C++ programming).

![Print](/media/img12.png)

* Unlike C programing language in case of printing the value of a variable, we just put the variable name into print methods parentheses:

``` Java
double pi = 3.14;
System.out.println(pi);
```

and the output will be:

``` Batch
3.14
```

* Strings can be concatenated with other strings or variables using `+` in print methods:

``` Java
int age = 18;
System.out.println("I'm " + age + " years old");
System.out.println("How" + " about you?");
```

the output will be:

``` Batch
I'm 18 years old
How about you?
```

* There are some control characters in printing formation that mostly come with the `\` symbol:

| Character | Output                |
| --------- | --------------------- |
| \n        | New line              |
| \\t       | tab                   |
| \\"       | Double quotation mark |
| \\'       | Single quotation mark |
| \\\       | Back slash sign       |
