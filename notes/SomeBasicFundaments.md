# Basic Java Fundaments

In this tutorial, I want to talk about some fundaments in java and we gonna see how exactly things are working in java programming.

## Run Java Code In Terminal

As we mentioned before, when we write a java code, a .java file will be created that contains a class inside it, now we want to see how exactly a java code is executed by the system.

As mentioned in _Intro_ lesson, java is a `WORA` (Write Once, Run Anywhere) language and it can be executed on any platform. Keep up with the tutorial to see how Java exactly makes this possible.

So go to your file explorer and find that "Hello World" program which we wrote in previous tutorials and it's located in an `src` folder. Then right-click in src and open the directory inside your computer terminal.

> If you are a Windows 10 (or previous versions) user, you need to use "Command Prompt" and find the src folder using some cmd commands:
>
>   1. Open cmd
>   2. Enter the drive which src is located in (example: `D:`)
>   3. Type "`cd`" followed by a space
>   4. Enter the address of the folder after the space (example: `cd Users\username\IdeaProjects`)

Then type this in terminal then hit enter("App" is my file name. you need to write yours):

``` batch
javac App.java
```

> Watch your spelling and letter cases!

### Java Compiler

`javac` (java compiler) is a tool in JDK that reads class and interface definitions, written in the Java programming language, from the first line to last and compiles them into bytecode class files. It can also process annotations in Java source files and classes.

### Bytecode

Bytecode is the intermediate representation of a Java program, allowing a JVM (Java Virtual Machine) to translate a program into machine-level assembly instructions. When a Java program is compiled, bytecode is generated in the form of a `.class` file. This .class file contains non-runnable instructions and relies on a JVM to be interpreted.

so after compiling your code, you'll see a .class file that has the same name as our .java file. Now it's time to use the java interpreter as `java` command to run our code and see the output.

![DotClassFile](/media/img04.png)

in the terminal window type this:

``` batch
java App
```

> In the second command you don't need to specify the file's format (~~java App.class~~)

![Output](/media/img05.png)

At this point we can understand why Java is a cross-platform language: Because every single .java file, needs to be converted into bytecode and bytecode acts the main role in running a java program, so we can run a java code on **any** device that runs JVM.
