# Inheritance and Polymorphism

In Java, it is possible to inherit attributes and methods from one class to another. We group the "inheritance concept" into two categories:

* **subclass**(child): the class that inherits from another class.
* **superclass**(parent): the class being inherited from.

To inherit from a class, we use the `extends` keyword:

``` Java
class Vehicle {
  protected String brand = "Lamborghini";        // Vehicle attribute
  public void start() {                          // Vehicle method
    System.out.println("Whoom, Whoom!");
  }
}

class Car extends Vehicle {
  private String modelName = "Reventon";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the start() method (from the Vehicle class) on the myCar object
    myCar.start();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```

* As we mentioned in the "Modifiers" chapter, we used `protected` access modifier for (brand) to allow Vehicle subclasses (Car) access.

## Inheritance Ban

If you don't want other classes to inherit from a class, use the final keyword:

``` Java
final class Vehicle {
  ...
}

class Car extends Vehicle {
  ...
}
```

The above code will generate an error: cannot inherit from final Vehicle.

## Polymorphism

Polymorphism means "many forms", and it occurs when we have many classes that are related to each other by inheritance.

As we said, Inheritance lets us inherit attributes and methods from another class. Polymorphism uses those methods to perform different tasks. This allows us to perform a single action in different ways.

For example, think of a superclass called Shape that has a method called shapeArea(). Subclasses of shape could be Square, Circle, or Triangle - And they also have their own implementation of area:

``` Java
class Shape {
  public void shapeArea() {
    System.out.println("The shape has an area");
  }
}

class Circle extends Shape {
  public void shapeArea() {
    System.out.println("Area = pi * radius * radius");
  }
}

class Square extends Shape {
  public void shapeArea() {
    System.out.println("Area = side * side");
  }
}
```

Now we can create square and circle objects and call _shapeArea()_:

``` Java
class Main {
  public static void main(String[] args) {
    Shape myShape = new Shape();     // Creates a Shape  object
    Circle myCircle = new Circle();  // Creates a Cricle object
    Square mySquare = new Square();  // Creates a Square object

    myShape.shapeArea();
    myCircle.shapeArea();
    mySquare.shapeArea();
  }
}
```

Outputs:

``` Batch
The shape has an area
Area = pi * radius * radius
Area = side * side
```
