# Packages and API

In Java, a package is used to group related classes. You can think of it as toolbox which we can use its stuff. We use packages to avoid name conflicts, and to write a better maintainable code. Packages are divided into two categories:

* Built-in Packages (packages from the Java API).
* User-defined Packages (create your own packages).

## Built-In Packages

The Java API is a library of prewritten classes, that are free to use, included in JDK (Java Development Kit). The library contains components for managing input, database programming, and much much more. The complete list can be found at [Oracle Website](https://docs.oracle.com/javase/8/docs/api/).

The library is divided into packages and classes. Meaning you can either import a single class (along with its methods and attributes), or a whole package that contain all the classes that belong to the specified package.

To use a class or a package from the library, you need to use the import keyword:

``` Java
import package.name.Class;   // Import a single class
import package.name.*;   // Import the whole package
```

## User-Defined Packages

To create your own package, you need to know that Java uses a file system directory to store them. Just like folders on your computer:

``` Batch
directory/mypackage/Main.java
```

To create a package, use the package keyword:

``` Java
package mypackage;
class Main {
  public static void main(String[] args) {
    System.out.println("This is my package!");
  }
}
```
