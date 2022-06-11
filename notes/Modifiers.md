# Java Modifiers

Modifiers are keywords that you add to your classes or methods or etc. to change their accessablity or funtionality.

We divide modifiers into two groups:

* **Access Modifiers**: Controls the access level
* **Non-Access Modifiers**: Do not control access level, but provides other functionality.

## Access Modifiers

For **classes**, we can use either `public` or `default`:

| Modifier  | Description                                                                                                      |
| --------- | ---------------------------------------------------------------------------------------------------------------- |
| `public`  | The class is accessible by any other class.                                                                      |
| `default` | The class is only accessible by classes in the same package.</br>This is used when you don't specify a modifier. |

For **attributes**, **methods** and **constructors**, you can use the one of the following:

| Modifier    | Description                                                                                          |
| ----------- | ---------------------------------------------------------------------------------------------------- |
| `public`    | The code is accessible for all classes                                                               |
| `private`   | The code is only accessible within the declared class.                                               |
| `protected` | The code is accessible in the same package and subclasses.                                           |
| `default`   | The code is only accessible in the same package.</br>This is used when you don't specify a modifier. |

> We'll talk about subclasses in upcoming tutorials.

## Non-Access Modifiers

For **classes**, we can use either `final` or `abstract`:

| Modifier   | Description                                                                                                        |
| ---------- | ------------------------------------------------------------------------------------------------------------------ |
| `final`    | The class cannot be inherited by other classes.                                                                    |
| `abstract` | The class cannot be used to create objects (To access an abstract class, it must be inherited from another class.) |

> We will learn more about inheritance and abstraction in upcoming tutorials.

For **attributes** and **methods**, you can use the one of the following:

| Modifier       | Description                                                                                                                                                                                    |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `final`        | Attributes and methods cannot be overridden/modified.                                                                                                                                          |
| `static`       | Attributes and methods belongs to the class, rather than an object.                                                                                                                            |
| `abstract`     | Can only be used in an abstract class, and can only be used on methods that does not have a body.</br>For example abstract void run();. The body is provided by the subclass (inherited from). |
| `transient`    | Attributes and methods are skipped when serializing the object containing them.                                                                                                                |
| `synchronized` | Methods can only be accessed by one thread at a time.                                                                                                                                          |
| `volatile`     | The value of an attribute is not cached thread-locally, and is always read from the "main memory".                                                                                             |
