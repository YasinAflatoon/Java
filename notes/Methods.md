# Methods

Methods are blocks of code that use some parameters and perform actions, so they are also called "Functions". We use methods to avoid repetition and use them in different parts of our code by calling them.

## Create a Method

a method must be declared within a class using the format below:

``` Java
public class App {
    public static void myMethod() {

    }
}
```

so just like that, we declared a method.

> Currently you don't need to know about the keywords "public", "static" and "void" you'll learn them eventually.

## Calling a Method

As we mentioned, methods can be called within our program so let's say we want to call a method that asks the user, his/her age:

``` Java
public class App {

    public static void main(String[] args) {
        howOld();
    }

    public static void howOld() {
        System.out.println("How old are you?");
    }
} // Outputs: How old are you?
```

So there are some points we need to notice:

* main itself, is a special method that works as our start point.
* A method cannot be declared inside another method but we can call one inside the other one ("main" and "howOld" for instance).
* A method can be called multiple times.

## Method Parameters

Parameters are pieces of information that can be passed to methods and they act as variables inside them. Parameters are specified after the method's name, inside the parentheses. We can add as many parameters as we want we just need to separate them with a comma.

``` Java
public class App {

    public static void main(String[] args) {
        howOld("Yasin");
    }

    public static void howOld(String name) {
        System.out.println("How old is " + name + "?");
    }
} // Outputs: How old is Yasin?
```

As you see, our "howOld" method, has one String-type parameter (name) which tells us that we should call this method with a String value (Yasin).

> When a parameter is passed to the method, it is called an argument. So, from the example above: "name" is a parameter, while "Yasin" is an argument.

We have the same formula for calling multiple parameter methods. The thing we should notice is to call our method with the same argumant type and order as parameters:

``` Java
public class App {

    public static void main(String[] args) {
        howOld("Yasin", 19);
        howOld("Jane", 23);
        howOld("Jesse", 26);
    }

    public static void howOld(String name, int age) {
        System.out.println(name + " is " + age);
    }
}
```

The output will be:

``` Batch
Yasin is 19
Jane is 23
Jesse is 26
```

## Return Values

So we know that methods act like a factory that uses some materials to give us a final product so they return us something. The `void` keyword we've used in this tutorial, so far indicates that our method should not return a value. if you want your method to return a value you need to replace "void" with a variable (int, char, string, etc.)

| Return Type | Description                             |
| ----------- | --------------------------------------- |
| void        | Makes the method not return a value. |
| byte        | Makes the method return a byte value.   |
| short       | Makes the method return a short value.  |
| int         | Makes the method return an int value.    |
| long        | Makes the method return a long value.   |
| float       | Makes the method return a float value.  |
| double      | Makes the method return a double value. |
| String      | Makes the method return a String value. |

> Methods can have either 0 (void) or 1 (non-void) return value.

So let's say we want to have a method that calculates the average of 3 integers:

``` Java
public class App {
    public static void main(String[] args) {
        System.out.printf("%2.2f", average(28, 41, 26));
    }

    public static double average(int numOne, int numTwo, int numThree) {
        return (numOne + numTwo + numThree) / 3.0;
    }
} // Outputs: 31.67
```

> We use 3.0 instaed of 3 to specify that the result of "(numOne + numTwo + numThree) / 3.0" must be a double-type value.
> You can think of methods as a variable that stores its return type. -> _average(28, 41, 26)_ is a double.

## Method Overloading

Method overloading means that we can have methods with the same name but different parameters. This helps us to create different methods with different parameter types but call the method with a shared name:

``` Java
public static void main(String[] args) {
    System.out.println("int: " + plusMethod(8, 5));
    System.out.println("double: " + plusMethod(4.3, 6.26));
}
    
static int plusMethod(int x, int y) {
    return x + y;
}

static double plusMethod(double x, double y) {
    return x + y;
}
```

So as you see we used method overloading to avoid using different names for methods that do the same thing but have different parameter types.

## Scope

In Java, variables are only accessible inside the region they are created. This is called `scope`.

### Method Scope

Variables declared directly inside a method are available anywhere in the method following the line of code in which they were declared.

### Block Scope

A block of code refers to all of the code between curly braces `{}`.

Variables declared inside blocks of code are only accessible by the code between the curly braces, which follows the line in which the variable was declared.
