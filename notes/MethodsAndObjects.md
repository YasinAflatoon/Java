# Methods and Object

In this tutorial we're going to talk more specifically, about methods and how they are related to objects.

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

As you can see, we created the program for a car which has only two methods "brake" and "shiftGear" and we created an object "pagani zonda" which can use these two methods.
