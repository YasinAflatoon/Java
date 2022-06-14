# Abstraction

Data abstraction is the process of hiding certain details and showing only essential information to the user.
Abstraction can be achieved with either **abstract classes** or **interfaces**.

As we learned, the `abstract` keyword is a non-access modifier, used for classes and methods:

**Abstract class:** is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).

**Abstract method:** can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from).

``` Java
abstract class Animal {
  public abstract void animalSound();
  public void sleep() {
    System.out.println("Zzz");
  }
}
```

* An abstract class can have both abstract and regular methods.
* It's not possible to create an object of the Animal class:

``` Java
Animal myObj = new Animal(); // will generate an error
```

* To access the abstract class, it must be inherited from another class.

We use abstraction to achieve security and hide certain details and only show the important details of an object. Abstraction can also be achieved with Interfaces.

## Interfaces

An `interface` is a completely "abstract class" that is used to group related methods with empty bodies:

``` Java
// interface
interface Car {
  public void brake();   // interface method (does not have a body)
  public void clutch();  // interface method (does not have a body)
}
```

To access the interface methods, the interface must be "implemented" (kinda like inherited) by another class with the `implements` keyword (instead of `extends`). The body of the interface method is provided by the "implement" class:

``` Java
// interface
interface Car {
  public void brake();   // interface method (does not have a body)
  public void clutch();  // interface method (does not have a body)
}

// Ford "implements" the Car interface
class Ford implements Car {
  public void brake() {
    // The body of brake() is provided here
    System.out.println("Car speed reduces");
  }
  public void clutch() {
    // The body of cutch() is provided here
    System.out.println("Ready to shift gear.");
  }
}

class Main {
  public static void main(String[] args) {
    Ford mustang = new Ford();  // Create a Ford object
    mustang.brake();
    mustang.clutch();
  }
}
```

* Like abstract classes, interfaces cannot be used to create objects (in the example above, it is not possible to create a "Car" object in Main).
* Interface methods do not have a body - the body is provided by the "implement" class.
* On implementation of an interface, you must override all of its methods
* Interface methods are by default abstract and public
* Interface attributes are by default public, static and final
* An interface cannot contain a constructor (as it cannot be used to create objects)

> Java does not support "multiple inheritance" (a class can only inherit from one superclass). However, it can be achieved with interfaces, because the class can implement multiple interfaces.

To implement multiple interfaces, separate them with a comma:

``` Java
interface FirstInterface {
  public void myMethod(); // interface method
}

interface SecondInterface {
  public void myOtherMethod(); // interface method
}

class TempClass implements FirstInterface, SecondInterface {
  public void myMethod() {
    System.out.println("Some text..");
  }
  public void myOtherMethod() {
    System.out.println("Some other text...");
  }
}

class Main {
  public static void main(String[] args) {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}
```
