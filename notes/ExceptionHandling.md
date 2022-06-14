# Exception Handling

When executing Java code, different errors can occur: coding errors made by the programmer, errors due to wrong input, or other unforeseeable things.

When an error occurs, Java will normally stop and generate an error message. Technically Java will throw an exception (throw an error).

## try and catch

* The `try` statement allows you to define a block of code to be tested for errors while it is being executed.
* The `catch` statement allows you to define a block of code to be executed if an error occurs in the try block.

The try and catch keywords come in pairs:

``` Java
try {
  //  Block of code to try
}
catch(Exception e) {
  //  Block of code to handle errors
}
```

As an example, we want to use try and catch to handle this error:

``` Java
public class Main {
  public static void main(String[ ] args) {
    int[] myNumbers = {1, 2, 3};
    System.out.println(myNumbers[10]); // error!
  }
}
```

Outputs:

``` Console
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 10 out of bounds for length 3
    at App.main(App.java:4)
```

To prevent our program from showing this error, we can use exception handling:

``` Java
public class Main {
  public static void main(String[ ] args) {

    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    }
  }
} // Outputs: Something went wrong.
```

## finally

The `finally` statement lets you execute code, after try...catch, regardless of the result:

``` Java
public class Main {
  public static void main(String[ ] args) {

    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    }
    finally {
        System.out.println("Exception handled successfully.");
    }
  }
}
```

Outputs:

``` Console
Something went wrong.
Exception handled successfully.
```
