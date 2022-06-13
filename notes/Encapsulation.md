# Encapsulation

In programming, encapsulation means hiding "sensitive" data from users. to do that we must:

* declare class attributes as `private`
* provide public get and set to access and update the value of a private variable.

## Get and Set

We learned from the previous tutorial that private variables can only be accessed within the same class (an outside class has no access to it). However, it is possible to access them if we provide public `get` and `set` methods.

The **get** method, returns the variable value, and **set** method sets the value.

The syntax for both is that they start with either get or set, followed by the name of the variable, with the first letter in upper case:

``` Java
public class Account {
  private String username; // private = restricted access

  // Getter
  public String getUsername() {
    return username;
  }

  // Setter
  public void setUsername(String newUsername) {
    this.username = newUsername;
  }
}
```

* The get method returns the value of the variable _username_.
* The set method takes a parameter (newUsername) and assigns it to the username variable. The `this` keyword is used to refer to the current object.

As we mentioned before, we cannot have access to private attributes from another class, but using get and set, helps us to do that:

``` Java
public class Main {
    public static void main(String[] args) {
        Account obj = new Account();
        obj.setUsername("YasinAflatoon"); // This will set username to: YasinAflatoon
    }   
}
```

## Why Encapsulation?

* Better control of class attributes and methods.
* Class attributes can be made read-only (if you only use the get method), or write-only (if you only use the set method).
* Flexibility: the programmer can change one part of the code without affecting other parts.
* Increased security.
