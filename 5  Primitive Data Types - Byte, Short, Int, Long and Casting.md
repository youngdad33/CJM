The `int` isn't the only type of whole number variable available in Java (or programming in general). In total, there are four types of whole number Variable: `byte`, `short`, `int` and `long`.

Each Variable type are different sizes. In the previous note, I mentioned that the Variable is a type of box. Now think about different size boxes. The `byte` is the smallest type of Variable. The `long` is the biggest.

##The `byte`:

In programming, we need to be careful of memory management. Fortunately, one of the advantages of Java (as mentioned in [1: Java - Introduction](quiver:///notes/3D0A27A5-B8DD-416D-BFB8-68A0A87B5714)) is that it takes care of memory management for us. However, if programming for platforms with smaller storage, making your package as small as possible is best practice. So why use large boxes for small items?

A `byte` as a memory width of **8 bits**. This makes it the smallest Variable available. This also means that the numbers it can contain are relatively small. The range of a `byte`is from **-128 to 127**. Anything bigger, and the compiler will throw an error.

```java
// Proper byte implementation
byte myByte = 127;

// Incorrect byte implementation
byte myByte = 129;
```

This simple code cell can't show an error, but on a compiler, it would look like this:

![Screen Shot 2017-07-17 at 00.08.01.png](resources/9EAA5A13760C3743F21C240E80221BC2.png =720x145)

This shows what the compiler on the command line will display. It's not exactly clear (it doesn't say "Your value is too large for type byte") but it does hint at what the problem is. The error reads 

>Error:(6, 28) java: incompatible types: possible lossy conversion from int to byte

This is saying "You've declared a byte, but you've assigned it the value of an int. I'll talk more about this later with Casting.

IntelijIDEA also gives a handy hint in the coding window when your value is too high for a `byte`.

![Screen Shot 2017-07-17 at 00.13.21.png](resources/82652A4C2008E6BD060322AFA5F125C8.png =431x110)

You'll notice here that the entire line of code is highlighted with a squiggly red line (like a spelling mistake in Word). If you hover your cursor over it, you'll see that it comes up with much the same message as the Command Line. It says that it requires a `byte` but it found an `int`.

##The `short`:

The `short` is the second variable. It is twice the size of the `byte`, which means it's memory width is **32 bits**. This means it can hold much larger numbers. In fact, the `short` has a range from **-32768 to 32767**.

The same thing will happen with the `short` as happened with the `byte` if you try to put a number too large. The compiler will throw an error and give much the same message. Fortunately, IntellijIDEA is there to help you too.

##The `int`:

We've already spoken about the [`int`](quiver:///notes/628A9CA0-D218-407F-B9CF-D669C2004D6D), so I'll only mention that the `int` is **32 bits** wide and has a range of **-2,147,483,648 to 2,147,483,647**.

##The `long`:

The `long` is the largest Variable available. It has  a memory width of **64 bits**, which gives it a range of **-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807** (9 Quintilion?).

When using `long` you have to add the letter L after the number to tell the computer/compiler you're using a `long`. It doesn't matter if it's an upper case `L` or lower case `l`, but it's best practice to use a `L` because it's easier to read in the code.

## Casting:

There is one problem with the `byte` and the `short` when it comes to operations.

When you try to add them to another Variables declaration, Java will automatically change them to an `int`. "No problem!", you may say, "The int is larger than both!". The problem is, you can't fit an `int` into either a `byte` or a `short`.

```java
// using byte or short for operations
byte myByte=4;
byte myByte2 = 4 + myByte;
```

This is the following error:
![Screen Shot 2017-07-17 at 00.08.01.png](resources/9EAA5A13760C3743F21C240E80221BC2.png =720x145)

Exactly the same as trying to fit a higher number into a `byte` or `short`. The reason is that Java changes whatever is on the right side of the assignment operator into an int **unless** you specifically tell it not to. This is called **Casting**. To cast a number, you simply put the Variable you want to force Java to use before the operation:

```java
// Casting
byte myByte = 4;
byte myByte2 = (byte) 4 + myByte;
```

The `(byte)` just after the assignment opperator will force Java to treat that as a `byte` and not automatically change it to an `int`.

When using a `long` or an `int`, you don't have to cast it, as Java automatically changes everything on the right of the assignment operator to an `int`, and a `long` can comfortably hold an `int`, so the compiler will not throw an error.