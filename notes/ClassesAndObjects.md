# Classes and Objects

Everything in Java is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.

A Class is like an object constructor or a "blueprint" for creating objects.

## Create a Class

As we mentioned before, to create a class, we use the `class` keyword. Let's say that we want to create a class called "Main" that contains the variable "x":

``` Java
public class main {
    int x = 8;
}
```

> A class should always start with an uppercase first letter, and the name of the java file should match the class name.

## Create an Object

In Java, an object is created from a class. We have already created the class named "Main", so now we can use this to create objects.

To create an object of Main, specify the class name, followed by the object name, and use the keyword new:

``` Java
public class main {
    int x = 8;

    public static void main(String[] args) {
        Main myObject = new Main();
    }
}
```

So now, we have an object which we can use to access attributes in class "Main".

## Using Multiple Classes

We can also create an object of a class and access it in another class.

> This is often used for better organization of classes (one class has all the attributes and methods, while the other class holds the main() method (code to be executed)).

Imagine we have two classes: "Main" and "Second" in the same directory. We can create an object of "Main" inside class "Second" and access attributes in "Main".

``` Java
public class Main {
    int x = 8;
}
```

``` Java
public class Second {
    public static void main(String[] args) {
        Main myObject = new Main();

        System.out.println(myObject.x);
    }
}
```

## Class Attributes

In the previous section, we used the term "variable" for x in the example. But x is actually an attribute of the class. Or you could say that class attributes are variables within a class:

``` Java
public class Main {
  int x = 8;
  int y = 10;
}
```

So now we call x and y, `attributes` of class "Main".

> Another term for class attributes is fields.

### Accessing Attributes

To access attributes of a class, we need to create an object of that class and use dot (`.`) syntax.

``` Java
public class Main {

    int x = 8;

    public static void main(String[] args) {
        Main obj = new Main();

        System.out.println(obj.x);
    }
} // Outputs: 8
```

As you see, we used _object_ "obj" to access _attribute_ "x" which is located in _class_ "Main".

* We can also modify attributes' values using the same formula:

``` Java
obj.x = 29;
```

#### final

We can use the keyword `final` to avoid overriding attributes:

``` Java
public class Main {

    final double pi = 3.14159;

    public static void main(String[] args) {
        Main obj = new Main();
        obj.pi = 3.14; // Will generate an error: Cannot assign a value to a final variable

        System.out.println(obj.pi);
    }
} // Outputs: 8
```
