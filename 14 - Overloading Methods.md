Now you know how to use methods, and how to make them return a value, another useful feature of methods to learn is how to Overload a method.

This doesn't mean breaking them and making them explode, rather using the same method using different parameters. This is a useful feature that allows you to keep your code count low, as well as your code neat.

To overload a method, you simply use the same name, but change the signature of it to accept different parameters. Return type (`void` or `int`), visibility (`public` or `private`), variable name and execptions it can throw are not part of the Method Signature. This means, the things we can change are:
* Different data type
* different number of variables
* different order of variables

```java
package com.DominicRoss;

public class Main {

    public static void main(String[] args) {
    
    }

    public static double calcFeetAndInchesToCentimeters (double feet, double inches){
         if(feet >=0 && inches >=0 && inches <=12){
             double totalInches= (feet * 12) * 2.54;
             totalInches += inches * 2.54d;
             return totalInches;
        }
        return -1;
  }
}
```

Here, I've created a Method in the same way we created a Method in the previous notes. This Method converts feet and inches into centimeters, it accepts two parameters - feet and inches as doubles.

Now, I'm going to use another mehtod with the same name, but with different parameters to overload it.

```java
package com.DominicRoss;

public class Main {

    public static void main(String[] args) {
        
    }

    public static double calcFeetAndInchesToCentimeters (double feet, double inches){
         if(feet >=0 && inches >=0 && inches <=12){
             double totalInches= (feet * 12) * 2.54;
             totalInches += inches * 2.54d;
             return totalInches;
        }
        return -1;
  }

    public static double calcFeetAndInchesToCentimeters(double inches){
        if (inches >=0){
            double feetInInches = (int) inches / 12;
            double remainingInches = (int) inches % 12;
            return calcFeetAndInchesToCentimeters(feetInInches, remainingInches);
        }
        return -1;
    }
}

```

As you can see, the second Method on Line 18 has exactly the same name (which you must be careful of to overload the method, not make a new Method with a slightly different name), except this method has only one parameter, inches. In this method, you can use a different calculation which is still relevant to the original method using different parameters.

In this second method, I've gone one further and called the first method to pass data into it. The second methods return, is the result of the first method. This means we are feeding our result from the second method as the arguments for our first method, which will, on completion, return the value of it's calculation as the return of the second method. Or, to put it a little simpler, the return of the second method is using the first method to calculate inches into centimeters.

Although this example is a little convoluted, Overloading Methods is a normal procedure in Java.