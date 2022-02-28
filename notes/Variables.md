# Java Variables

`Variables` are basically little containers where we can store data or pieces of information in our Java programs. In programming, we're actually working with a lot of data, and pieces of information like numbers or texts. These data need to be stored in these containers, so we can use them in different parts of our program.

## Data Types

There are two data types in Java language: `Primitive` and `Non-Primitive`

### Primitive Data Type

In Java, the primitive data types are predefined. They specify the size and type of any standard values. Java has 8 primitive data types namely `byte`, `short`, `int`, `long`, `float`, `double`, `char`, and `boolean`.

#### byte

The byte data type is a signed integer based on the two's complement 8-bit mechanism. The values that can be stored in a single byte range from -128 to 127.

#### short

The short data type is a signed integer based on the two's complement 16-bit mechanism. The values that can be stored in a single short variable range from -32,768 to 32,767.

#### int

The int data type is a signed integer based on the two's complement 32-bit mechanism. The values that can be stored in a single short variable range from -2,147,483,648 to 2,147,483,647.

> Basically int data type has the most usage for holding integers and in small scales, it doesn't really matter if you use int instead of short or byte.

#### long

The long data type is a signed integer based on the two's complement 64-bit mechanism. The values that can be stored in a single long variable range from -(2^63) to 2^63 - 1.

#### float

The float data type is a signed decimal number which is 6 decimal digits accurate.

#### double

The double data type is a signed decimal number which is 15 decimal digits accurate.

> double is the primary data type for decimal numbers.

#### char

The char data type is for holding one single character that you can type through your keyboard.

#### boolean

The boolean data type is for holding only two values of `true` or 'false'.

### Non-Primitive Data Type

Non-primitive data types in Java are not predefined. They are created by programmers. Non-primitive data types are also called 'reference variables' or 'object references' as they reference a memory location where data is stored. Some of the examples of non-primitive types include `strings`, `arrays`, and `classes`.

> We already know about class definition we head to the other two.

#### String

The string data type is actually a combination of characters that can be stored in ram.

#### Array

The array data type is used for saving two or more data types in one variable and they all share the same name but have a unique index.

> * String is actually an array of char.
> * We'll talk about arrays in the next tutorials.

## Define a Variable

So now we know different data types, it's time to declare them in our programs. To define a variable we need to:

1. Specify the data type.
2. Give our variable an appropriate name.
3. Put a semicolon at end of the line.

Now our variable is created in ram but it doesn't contain any data or value so we need to initialize it. To initialize variables may be a bit tricky and differ from one data type to another.

## Initializing

Initializing method for mentioned data types is kinda the same. first, you declare them then, follow the pattern below.

``` Java
byte age = 10;
short height = 180;
int telphone = 70262543;
long phoneNumber = 40123348701L;
double bmi = 18.27837423;
float score = 16.32F;
char grade = 'B';
boolean isMale = true;
String address = "No. 32, liberty street"; 
```

As you may notice initializing pattern is easy to follow you only need to put an equal sign and then set a value and end the line with a semicolon. But there are some points:

* In case of using long or float data type you need to put letters 'L' as long and 'F' as a float between the number you assign to variable and semicolon.

> The reason behind this act, is because Java automatically knows all decimal numbers as double and the same for int in integers. So we put these letters to specify them.

* In char initialization, you need to put the character between two single quotation marks. But for strings, we should put the phrase between double quotations.

## Variable Naming

Variable naming is an important aspect of making your code readable. Naming variables follow a simple idea: Create variables that describe their function and which follow a consistent theme throughout your code. Let’s take a look at some naming conventions:

### Snackecase

Words are delimited by an underscore.

``` Java
variable_one
variable_two
```

### Pascalcase

Words are delimited by capital letters.

``` Java
VariableOne
VariableTwo
```

### Camalcase

Words are delimited by capital letters, except the initial word.

``` Java
variableOne
variableTwo
```

Consistency and readability are key ideas that should be utilized in the naming of variables and these conventions help you with this. Regardless of how you choose to name your variables, always ensure that your naming conventions are consistent throughout the code. Consistency allows others to understand your code easily.
