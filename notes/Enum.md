# Enum

Enum is a special "class" that represents a group of constants (unchangeable variables, like final variables).

> Enum is short for "enumerations", which means "specifically listed".

To create an enum, use the `enum` keyword (instead of class or interface), and separate the constants with a comma. Note that they should be in uppercase letters:

``` Java
enum TrafficLight {
  RED,
  YELLOW,
  GREEN
}
```

* We can also have an `enum` inside a class.

``` Java
public class Main {
    enum TrafficLight {
  RED,
  YELLOW,
  GREEN
}
  public static void main(String[] args) {
    TrafficLight boulevard = TrafficLight.GREEN;

    switch(boulevard) {
      case RED:
        System.out.println("You can't cross the street");
        break;
      case YELLOW:
         System.out.println("Clear the street");
        break;
      case GREEN:
        System.out.println("You can cross the street");
        break;
    }
  }
}
```

* You can access enum constants with the dot syntax.

``` Java
TrafficLight.GREEN;
```
