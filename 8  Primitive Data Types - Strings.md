So far, as the titles suggested, I have been talking about Primitive Data Types - Variables. The eight Variables we have learnt so far are the `int`, the `byte`, the `short`, the `long`, the `float`, the `double`, the `char` and the `boolean`. There are two types of Data Type: The Reference Data Type and the Primitive Data Type. Reference Data Types refer to objects (something I'll talk about later). The Primitive Type directly contain values.

There is one more Data Type I need to talk about, and it's a bit of a hybrid. It is actually a `class`, but can also be thought of as a Primitive Data Type. That's because it can be highly evolved, or rather 'dumb'. The following will explain better:

```java
String myString = "This is a string";
```

We've already seen this use of the string in the [Hello World App](quiver:///notes/E70F4789-E4C6-485B-9DFE-1EB1D9EA2B5C) we built earlier. What I didn't meantion is that `String`s can be added to as the program continues.

```java
String myString = "This is a string";
myString = myString + ", and this is more text in the string";
System.out.println(myString);
```

If we run this in the Command Line, we get the following:

![Screen Shot 2017-07-19 at 23.17.35.png](resources/84BD50840D933D4E2053B9C63EA61DA3.png =409x94)

As you can see, adding to the string mid program just concatenates the two strings into one.

A `String` can contain any kind of character like letters, numbers and Unicode Characters (much like the `char`, but with  space for more than one character).

```java
String numberString = 33;
numberString = numberString + 33;
```

Now, what will this do? Will it add the two 33's together to make 66, or will it concatenate them together like the strings above? If we run this through the compiler, this is what is printed on the Command line:

![Screen Shot 2017-07-19 at 23.19.14.png](resources/DAF00D06118A82E38A4CA49DEC049752.png =409x108)

Here, you can see that it didn't add the two 33's together, just concatenated them. This is because a `String` is not designed for mathematical operations (at least, not in this state).

What happens if we add an `int` to a `String`? Will that resolve the issue because we're now using a Number Variable and adding it to a `String`?

```java
String lastString = "10";
int myInt = 10;
lastString = lastString + myInt;
System.out.pringln(lastString):
```

The answer is... No.

![Screen Shot 2017-07-19 at 23.20.47.png](resources/A366CD3A397C86523F84C13DB0B1C1B8.png =409x94)

Once again, the `int` and the `String` have been concatenated. This is because we are using a `String` on the left hand side of the assignment operator, so Java will automatically convert anyting on the right hand side to a string too.

This is what I meant when I said that a `String` can be either quite evolved or quite dumb. In this form, it's quite dumb and acting like a Primitive Data Type. Later, I'll explain how you can use a `String` more like a class and add characters halfway between words, remove certain words or characters and more.