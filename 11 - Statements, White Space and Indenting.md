#Statements:
In the [previous](quiver:///notes/28872197-A10B-4E0E-8E80-A7FCEF1F8E4E) note, I talked about Expressions, and briefly mentioned that the formed part of the Statement. So what is a Statement? A Statement is the entire line an Expression is in.

```java
int myInt = 4;
```

Here, the entire of line 1 is a statement. Here are some other Statements:

```java
int myInt = 4;
if(myInt >= 4){
    System.out.println("myInt is equal to " + myInt);
}
```

In this code example, lines 1-3 are statements.

You'll notice that Statements tend to end with a `;`. This is true in most cases, but there are some exceptions which I will discuss later.

#White Space:
White Space in coding is literally talking about the spaces in the code. Java, unlike some programming languages, doesn't take any notice of White Space. So:

```java
int             myInt               =           4           ;
```

Is the same as:

```java
int myInt = 4;
```

Or:

```java
int myInt=4;
```

Obviously, the middle option with some White Space is easier to read to us, but Java doesn't care.
> Note that there does have to be some White Space, for example between the Keyword and the Variable name, otherwise Java won't be able to understand what you're defining. So `intmyInt=4;` won't work, because the `int` isn't clearly defined for Java to find.

#Indentation:
Indenting code is an important step to making your code readable for other coders, as well as yourself. Although Java doesn't take any notice of Indentation, you'll find it's a lot easier to read:

```java
int myInt = 4;
if (myInt == 4){
    System.out.println("myInt is equal to " + myInt);
    if (myInt == 5){
        System.out.println("Nope!");
    }
}
```

Than:

```java
int myInt = 4;
if (myInt == 4){
System.out.println("myInt is equal to " + myInt);
if (myInt == 5){
System.out.println("Nope!");
}
}
```

In the second example, it's harder to see where the first `if` statement ends and the second begins (or if they're nested at all), where as the first example makes it clear that the second `if` statement is nested within the first.