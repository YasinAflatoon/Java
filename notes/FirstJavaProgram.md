# First Java Program

After JDK and IDE setup it's time to write your first java program.

## Lets Start

open your IDE. if you are a first-timer don't get intimidated by too many options you'll see in IDE.

Now click on `Files` and create a "New Project". In `IntelliJ` it will ask you to put a name for this project and choose a location for saving it. and in other IDEs, it will be the same.

When you create a project the IDE will create some folders in its default location which keeps all your codes and stuff, and in this folder, there is a subfolder called `src`. src is basically like a root directory to your source code where all your packages and classes are stored in it.

### Package

And you'll gonna see something else as "base Package". You're gonna see this word a lot when you are dealing with Java, which is "`Package`" and package is basically a special type of folder that stores similar Java files.

The package name is usually the organization's or person's domain name in reverse. In my case, it would be: "com.YasinAflatoon" and this package should be declared in the first line of your Java program.

> Using Package is not necessary but it will help you to specify your code from dozens of java codes, specially in codes that may be uploaded on a network.

### Class

To write our first Java program, we need to create something called `class` and class is basically just a special container that we use to store our java code.

So right-click on your _src_ folder, click on 'New', and click on "Java Class" or similar options in the IDE you're using.

At this moment you'll need to name your first Java class. I'm just gonna call it "App". then hit enter.

then you'll see a new tab in your IDE like this:

![FirstEncounter](/media/img01.png)

currently, you see the "App" class and a `.java` file which has the same name.

as I mentioned before, class is a container for our code. so everything should be written inside those curly braces of `public class App`.

Now to get started with Java, we actually have to create something called a `main method`.

> Don't worry too much about what a method is, we'll talk about that in upcoming tutorials.

This method is actually a little container that we can put inside of our class, where we can store all the codes that we want to execute.

> In Java programming, everything inside the main method is gonna get executed so this method acts as a start point for your app.

 let's do it. hit enter after the first curly brace, then on a new line type the below code:

``` Java
public static void main(String[] args) {

} 
```

Currently, you don't need to worry about those phrases `public`, `static`, `void`, you are gonna learn them all. Just for now, just know that our main method should be written like the above code.

Then inside the main method write this code:

``` Java
System.out.println("Hello, World!");
```

> * `System.out.println` (read print line) is actually a command that prints something for us in the console.
> * In Java every time you write a command you need to put a semicolon ( ; ) at the end of the line.

In IntelliJ, you will see a green "play" button next to the line number that you defined your class in. So click on it and your first java program will work for you if you just go as the tutorial.

![Result](/media/img02.png)

Congrats! you just wrote your first Java program!
