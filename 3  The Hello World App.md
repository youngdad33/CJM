Hello World is the most popular and basic first program that is tought to new students. All it does is print a line on the standard output (usually the Terminal window).

There is only 5 lines of code, so the code is very basic but also the most fundamental of any program. The following is the code of "Hello World" program:

```c
/**
*The HelloWorldApp class implements an application that
*simply Displays "Hello World!" to the standard output.
*/
class HelloWorldApp {
	public static void main(String[] args){
		System.out.println("Hello World!");// Display the String.
	}
}
```

Below I will break down the program to explain the individual elements of the program.

##Comments:

As in all programming languages, Comments are ignored by the compiler. They are, however, useful to leave yourself - and other coders - useful notes about the code.

In Java, there are 3 types of comments:
	* Multi line comment: `/* [text goes here] */` .
	* Documentation: `/** [Documentation] */` This is used for Doc Comment which the `javadoc` tool uses to prepare automatically generated documentation.
	* Single line Comment: `//[text goes here]`.

##Class Definition:

The `class HelloWorldApp {` is the beginning of the class definition of the Hello World App. The most basic form of class definition is `class [name]{...}`.
`class` is a keyword which tells the compiler what follows - like an HTML tag. The class' name follows. This can be anything you want (upper/lower case, numbers, _ and $ can be used in a name, but it is **CASE SENSITIVE**) , and allows you to code different classes for different things. All the code for that class shows inbetween the two curly braces.

##[Main Method:](quiver:///notes/FBB5AB59-DE38-4629-910E-0DDF2C8697F2)

Every Java Program must have a Main method. It can have many other methods, but one **must** be called main. If it doesn't, the program will not run. The `main` method is the entry point of your application and will subsequently invoke all other methods required by the program. The Main Method signature is:

`public static void main(String[] args){...}`

The main method must always be writen with this code. The modifiers `public` and `static` can be put round either way, but Java convention is `public static`.
The argument `args` can be named whatever you like, but again, Java convention is to call it `args` or `argv`.

The `main` mehtod accepts a single argument: an array of elements of type `String`. This is the way through which the runtime system passes information to your application. Each string in the array is called a **command-line argument**, which lets users affect the operation of the application without recompiling it. It would be possible, for example, for a sorting app to allow the user to specify the data is displayed in decending order using the command line argument `-descending`. This Hello World app doesn't use arguments, but you'll come across them in more complex apps.

##System:

The `System` class comes from the core library (or Aplication Programming Interface - API). This tells the program to print the "Hello World" to the standard output. In our case, at the moment, it's the terminal window we run it in.