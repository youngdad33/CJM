You now know two types of Control Flow (or Conditional Statement): The `if` and the `switch`. Now, you'll learn a third, the `for` statement or loop.

#The `for` loop:
The `if` and `switch` statements are good for testing conditions and executing code based on those conditions, but what if you need to reproduce the code a number of times? There are three options.

###Option 1 - duplicate the code:
The first obvious solution is to duplicate the code, but as you've already learnt, duplicating code is a bad way to program, as one syntax error will cause the whole thing to crash. So best not use this mehtod.

###Option 2 - use an `if` or `switch` statement:
This option is better, but not by much, as the code will have to be repeated numerous times to complete the same process. Also, the `if` and `switch` statements aren't designed to reproduce code numerous times. They are designed to execute code based on seperate parameters. Again, not the best solution.

###Option 3 - Use the `for` loop:
As the name suggests, the `for` loop is designed to loop numerous times executing the exact same code till a condition evaluates as false. If you have code to repeat, this is the guy for the job!

##Using a `for` loop:
To initialise a `for` loop, you need 3 things:
1. initialisation
2. termination
3. incrementation

This goes in the opening brackets of the `for` loop similar to the conditions of the `if` or `switch` statements.

```java
for (init; term; inc){
    //code here
}
```

##Initialisation:
To initialise the for loop, you need a variable to keep track of the amount of times the loop as executed. The most common way of doing that is with an `int` variable of `i` set to 0.

```java
for (int i = 0; term; inc){
    //code here
}
```

###Counting in programming:
When counting in programming, you - almost - always start at 0. That's because computers count 0 as a number, not the lack of a number. Humans consider 0 to be nothing. Computers consider it to be somthing. That's because to use 0, you still have to use memory. 0 in binary is 00000000.
> If you want to count nothing, you need to use the term `null`, which is a complete lack of data. 0 is still data.

##Termination:
The second part of the `for` loop condition is termination. That means you're telling the compiler where to stop looping. You need this to evaluate as flase for the loop to stop. As long as the termination is true, the loop will keep going.

```java
for (int i = 0; i <5; inc){
    //code here
}
```

##Incrementation:
The third and final part of setting the for loop is incrementation, or telling the compiler you have completed one loop.
> If this step is skipped, you'll fall in to an infinite loop, because the termination will never amount to false. This will mean the program will never stop compiling, and eat up a lot of memory and finally crash your device. Moral of the story: NEVER FORGET TO INCREMENT!!!

```java
for (int i = 0; i <5; i++){
    //code here
}
```

Now that you've set up the for loop, you can type the code inside that needs to be repeated. This will continue till the condition (the termination part of the set up) evaluates as false, after which the compiler will continue to the code bellow/outside the `for` loop.

#Example code:

```java
public class Main {

    public static void main(String[] args) {
	    //Using the for statement, call the calculateInterest method with
        // the amount at 10,000 with the interest rate of 2, 3, 4, 5, 6, 7 and 8
        // and print the results to the console window

        for (int i = 2; i < 9; i++){
            System.out.println("10,000 at " + i + "% interest = " + calculateInterest(10000, i));
        }

        // How would you modify the loop above to do the same thing as
        // shown but to start at 8% and work back to 2%
        System.out.println("*************");
        for (int i = 8; i > 1; i--){
            System.out.println("10,000 at " + i + "% interest = " + calculateInterest(10000, i));
        }

        // Create a for statement using any range of numbers
        // Determine if the number is a prime number using the isPrime method
        // if it is a prime number, print it out AND increment the count of the
        // number of prime numbers found
        // If that count is 3 exit the for loop
        // hint: Use the break; statement to exit
        System.out.println("***************");

        int primeCount = 0;
        for (int i = 77; primeCount <= 2; i++){
            if (isPrime(i)){

                System.out.println(i + " is a prime number");
                primeCount++;
            }
        }
    }

    public static boolean isPrime(int n){
        if (n == 1){
            return false;
        }
        for (int i = 2; i <= n/2; i++){
            if (n % i == 0) {
                return false;
            }
        }
        return true;
    }

    public static double calculateInterest (double amount, double interestRate){
        return (amount * (interestRate/100));
    }
}
```