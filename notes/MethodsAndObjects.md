# Methods and Object

In this tutorial, we're going to talk more specifically, about methods and how they are related to objects.

## static and non-static

You will often see Java programs that have either static or public attributes and methods. So simply, an `static` method is a method that can be accessed without creating an object of the class, unlike `public` which can only be accessed by objects.

``` Java
public class Main {
    public static void main(String[] args) {
        methodOne();
     // methodTwo(); This will generates an error: Non-static method cannot be referenced from a static context.

        Main obj = new Main();
        obj.methodTwo();
    }

    static void methodOne() {
        System.out.println("Static methods can be called without creating objects");
    }

    public void methodTwo() {
        System.out.println("Public methods must be called by creating objects");
    }
}
```

### Access methods by objects

In this example we want to create class "Car" and write some methods for that and access these methods by an object:

``` Java
import java.util.Objects;

public class Car {
    public static void main(String[] args) {
        Car paganiZonda = new Car();
        paganiZonda.brake();
        paganiZonda.shiftGear("Down");

    }

    public void brake() {
        System.out.println("Car speed reduced.");
    }

    public void shiftGear(String upDown) {
        if (Objects.equals(upDown, "Up")) {
            System.out.println("Gear shifted up");
        } else System.out.println("Gear shifted down.");
    }

}
```

Outputs:

``` Batch
Car speed reduced.
Gear shifted down.
```

As you can see, we created the program for a car that has only two methods "brake" and "shiftGear" and we created an object "pagani zonda" which can use these two methods.

## Java Constructors

A constructor in Java is a special **method** that is used to initialize objects. The constructor is called when an object of a class is created. It can be used to set initial values for object attributes:

``` Java
public class Main {
    int x;  // Class attribte

    // Class Constructor:
    public Main() {
        x = 8;
    }

    public static void main(String[] args) {
        Main obj = new Main(); // This will call the constructor
        System.out.println(obj.x);
    }
} // Outputs: 8
```

* The constructor name must match the class name, and it cannot have a return type.
* All classes have constructors by default: if you do not create a class constructor yourself, Java creates one for you. However, then you are not able to set initial values for object attributes.
* Also note that the constructor is called when the object is created.

### Constructor Parameters

Constructors can also take parameters, which are used to initialize attributes.

``` Java
public class Main {
    int x;

    public Main(int value) {
        x = value;
    }

    public static void main(String[] args) {
        Main obj = new Main(8); // Initializes x to 8;
        System.out.println(obj.x);
        // Outputs: 8
    }
}
```

In the example above, when we call the constructor by "8", it sets _int value_ to 8 and then initializes _x_ by the same value.
