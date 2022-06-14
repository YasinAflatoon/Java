# Nested Classes

In Java, it is possible to nest classes (a class within a class). The purpose of nested classes is to group classes that belong together, which makes your code more readable and maintainable.

## Inner Classes

To access the inner class, create an object of the outer class, and then create an object of the inner class:

``` Java
class OuterClass {
  int x = 10;

  class InnerClass {
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}

// Outputs 15 (5 + 10)
```

* Unlike a "regular" class, an inner class can be private or protected. If you don't want outside objects to access the inner class, declare the class as private.
* An inner class can also be static, which means that you can access it without creating an object of the outer class.

> Just like static attributes and methods, a static inner class does not have access to members of the outer class.

* Inner classes, can access attributes and methods of the outer class.
