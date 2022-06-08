# Arrays

Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

To declare an array, define the variable type with square brackets:

Example:

``` Java
String[] friends;
```

We have now declared a variable that holds an array of strings. To insert values to it, we can use an array literal - place the values in a comma-separated list, inside curly braces.

``` Java
String[] friends = {"Joey", "Phoebe", "Monica", "Chandler", "Ross", "Rachel"};
```

The length of an array will be created once (when the array is initialized). So in previous example our array length is 6.

There is another method to declare an array and length without initialazing:

``` Java
String[] frineds = new String[6];
```

* You access an array element by referring to the index number:

``` Java
String[] friends = {"Joey", "Phoebe", "Monica", "Chandler", "Ross", "Rachel"};
System.out.println(friends[0]);
// Outputs: Joey
```

> Note: Array indexes start with 0: [0] is the first element. [1] is the second element, etc and ends with n-1 index (Ross is friends[5]).

* To change the value of a specific element, refer to the index number:

Example:

``` Java
String[] friends = {"Joseph", "Phoebe", "Monica", "Chandler", "Ross", "Rachel"};
friends[0] = "Joey";
// Now ouputs Joey instead of Joseph
```

* To find out how many elements an array has, use the `length` property:

``` Java
String[] friends = {"Joseph", "Phoebe", "Monica", "Chandler", "Ross", "Rachel"};
System.out.println(friends.length);
// Outputs: 6
```
