Here, I'm going to talk about two more data types available in programming. So far, I've talked about Variables for whole numbers - using the `byte`, the `short`, the `int` and the `long` - but now we move on to more precise numbers, namely decimal numbers. To deal with decimal numbers, there are two types of Variable available: The `float` and the `double`.

## The `float`:

The `float` is the basic form of decimal place number. It is much like the `int`, in that it has a width of **32 bits**, which means it has an acuracy of 7 (or seven numbers after the decimal point).

## The `double`:

The `double` is a more precise Variable for decimal place numbers. It has a width of **64 bits**, which means it has an acuracy of 16 (16 decimal places).

Look at the code example below:

```java
public static void main(String[] args) {
        //width if int = 32 (4 bytes)
        int myIntValue = 5;
        //width of float = 32 (4 bytes)
        float myFloatValue = 5f;
        //width of double = 64 (8 bytes)
        double myDoubleValue = 5d;
        
        System.out.println("myIntValue: " + myIntValue);
        System.out.println("myFloatValue: " + myFloatValue);
        System.out.println("myDoubleValue: " + myDoubleValue)
}
```

Here, I've used three values which will display the same number; a 5.

Note how the `float` has a `5f` and the `double` has a `5d` after the assignment operator. This is because Java will always assume/convert the number on the right of assignment operator to a `double`. To stop that, we can either cast the number as a `float` or `double` (see [5: Data Type Variables - Byte, Short, Int, Long and Casting:](quiver:///notes/3DE2EAF4-C889-45BB-91B1-E9879DB9C366) for casting) or we can add an `f` or `d` after the number, similar to how we added an `L` after a `long`.

If we were to run this code, we would get the following output on the Command Line:

![Screen Shot 2017-07-17 at 23.23.16.png](resources/FDD932D50CCE33E05AEDC2BBB180AFAB.png =169x78)
*Screenshot of Command line after using the above code*

You'll notice that the three lines show the expected result, but that both the `float` and the `double` show the number with a decimal place, even though we didn't add one.

Now, what would happen if we did some math with these numbers, for example:

```java
public static void main(String[] args) {
        //width if int = 32 (4 bytes)
        int myIntValue = 5/2;
        //width of float = 32 (4 bytes)
        float myFloatValue = 5f/2f;
        //width of double = 64 (8 bytes)
        double myDoubleValue = 5d/2d;
        
        System.out.println("myIntValue: " + myIntValue);
        System.out.println("myFloatValue: " + myFloatValue);
        System.out.println("myDoubleValue: " + myDoubleValue)
}
```

What will happen now? Will the `int` show the correct answer, or will it round it up/down?

The answer is shown in this screenshot from the Command Line:

![Screen Shot 2017-07-17 at 23.25.13.png](resources/4B35647A684F399555C8497F79CA3A16.png =172x80)
*Screenshot of Command Line after using the deviding code*

Here, you can clearly see that the `int` has ignored the remainder (the 0.5) and only shown a 2. This is because it doesn't handle decimal places, only whole numbers.

The `float` and the `double`, on the other hand, have shown the full answer of 2.5. Now lets see what happens if we program the code to devide by 3.

```java
public static void main(String[] args) {
        //width if int = 32 (4 bytes)
        int myIntValue = 5/3;
        //width of float = 32 (4 bytes)
        float myFloatValue = 5f/3f;
        //width of double = 64 (8 bytes)
        double myDoubleValue = 5d/3d;
        
        System.out.println("myIntValue: " + myIntValue);
        System.out.println("myFloatValue: " + myFloatValue);
        System.out.println("myDoubleValue: " + myDoubleValue)
}
```

![Screen Shot 2017-07-17 at 23.26.32.png](resources/1F9A4BD7F829C112340FCB36D0D1C1DE.png =253x83)
*Screenshot of Command line after deviding the code by 3*

Now we really see the `float` and the `double` come into play. Once again, the `int` has failed to show any of the remainders, as it's not designed to. The `float` is giving us up to 7 decimal place answer, but the `double` is much more accurate, showing up to 16 decimal places. But there are other advantages to using a `double` over a `float`:
1. The `double` is processed a lot quicker on modern computers than the `float`.
2. Java inbuilt mathematical equations (`sin`, `cos`, `cosin` etc) will retun their result as a `double`.
3. Because the `double` is more acurate.