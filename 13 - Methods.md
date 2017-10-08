You saw in lesson [12](quiver:///notes/029CE0D2-CFBF-416F-BBE8-CF61FCDCBC19) that to do multiple calculations on a code block with using the same values means not only overwriting the original vallues, but also retyping the code blocks as many times as the calculation is needed. This is cumbersome to the code, and makes it very long. The answer is methods. First of all, I'll recall the code we had in the previous lesson:

```java
public class Main {

    public static void main(String[] args) {
	    boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;

	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore);
        }
        
        score = 10000;
        levelCompleted = 8;
        bonus = 200;
        
        if(gameOver){
            int finalScore = score + (levelCompleted * bonus);
            System.out.println("Your Final Score was " + finalScore);
        }
    }
}
```

This is the same code we had in the previous lesson. There are 4 variables, and two code blocks doing the same thing, and in the middle, the variables are overwritten with new values. So how do we fix this with a Method? In fact, what is a Method?

You may not realise it, but you've been using a Method since the Hello World program. In the code above, line 3 is a method, the `public static void main(String[] args) {` is the Method. Remember when I was [explaining the code of the Hello World app](quiver:///notes/E70F4789-E4C6-485B-9DFE-1EB1D9EA2B5C), I said that every Java programme must have a `main` Method, as this is the main worker of your entire programme.

A Method is described as:
> ... a set of code which is referred to by name and can be called (invoked) at any point in a program simply by utilizing the method's name. Think of a method as a subprogram that acts on data and often returns a value. Each method has its own name.

So to run this code block, you're going to code a subprogram which you can then use when ever you want to run the calculation. First, start by defining the Method:

##The First Code Block:

```java
public class Main {

    public static void main(String[] args) {
	    boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;
	    
	    score = 10000;
        levelCompleted = 8;
        bonus = 200;
        
        if(gameOver){
            int finalScore = score + (levelCompleted * bonus);
            System.out.println("Your Final Score was " + finalScore);
        }
    }
    
    public static void calculateScore(){
        boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;

	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore); 
	    }
    }
}
```

Now, I've created a new method called `calculateScore` and I've added the first code block to it, and deleted the first code block from the beginning of the `main` Method. Now, when you want to use the `calculateScore` method, you simply call it using its name.

```java
public class Main {

    public static void main(String[] args) {
        boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;
	    
        calculateScore()
        	    
	    score = 10000;
        levelCompleted = 8;
        bonus = 200;
        
        if(gameOver){
            int finalScore = score + (levelCompleted * bonus);
            System.out.println("Your Final Score was " + finalScore);
        }
    }
    
    public static void calculateScore(){
        boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;

	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore); 
	    }
    }
}
```

Notice how when you call the method, you need to add a `;` to the end of the line. That's because it's the end of the operation.

When you compile the code, what will happen is Java will reach line 5, notice we're calling a new method and jump to line 17 where that Method is. It will run line 17-28, then return to where it left off on line 6 and continue running the rest of the `main` Method. The output will be the same as the first code block we ran, because nothing has changed, we've just moved the calculation to a new Method.

##Parameters:
What we need to do now is pass the Variables to the method, so that each time we use it, we can change the Variables without deleting the original values. We do this using **parameters**.

Parameters are what the method will use to complete the calculations inside it. We define Parameters inside the Method's parentheses.

```java
public class Main {

    public static void main(String[] args) {
	    boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;
	    
	    calculateScore();
	    
	    score = 10000;
        levelCompleted = 8;
        bonus = 200;
        
        if(gameOver){
            int finalScore = score + (levelCompleted * bonus);
            System.out.println("Your Final Score was " + finalScore);
        }
    }
    
    public static void calculateScore(boolean gameOver, int score, int levelCompleted, int bonus){
        boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;

	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore); 
	    }
    }
}
```

Now you've added parameters to the method, which means the method will expect some values to come in when called from the main to be able to perform the calculation. That is done using **Arguments**.

Before I move on to that, you'll notice that when you enter Parameters to the Method, InteliJ will tell you that you have an error, because your Method call has no arguments. The folowing screen shot will show you what this looks like:

![Screen Shot 2017-07-27 at 00.09.47.png](resources/91974358E3826E34D9DDF2B04001A75A.png =712x298)

This is the IDE saying that the Method is expecting values, but none have been set.

##Arguments:
To pass the values to the Method, you use Arguments. Again, you have seen Arguments since the Hello World app in the `main` Method. The `(Strings[] args)` line at the end of the Method signature is a reminder that the `main` Method takes arguments of type string.
So in our code, we need to add the values in to the Method Call by adding them in between the parentheses. Remember, (in this code) the Method is expecting a `boolean` and three `int`.

```java
public class Main {

    public static void main(String[] args) {
	    boolean gameOver = true;
	    int score = 800;
	    int levelCompleted = 5;
	    int bonus = 100;
	    
	    calculateScore(true, 800, levelCompleted, bonus);
	    
	    score = 10000;
        levelCompleted = 8;
        bonus = 200;
        
        if(gameOver){
            int finalScore = score + (levelCompleted * bonus);
            System.out.println("Your Final Score was " + finalScore);
        }
    }
    
    public static void calculateScore(boolean gameOver, int score, int levelCompleted, int bonus){
	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore); 
	    }
    }
}
```

I've now added the arguments to the Method Call, and this has allowed me to remove the Variables from the Method. That's because when you create Parameters, Java will automatically create the Variables you define and delete them once the Method has completed (much like the `finalScore` Variable we created inside the method).

You'll also notice that in the Method call, I've put half values (true and 800) and half Variables (levelCompleted and Bonus). This is fine to code, as you're sending the Arguments needed to complete the Method call. However, this only works if the Variables have already been defined.

##The Second Code Block:
So how do we complete the second code block? Do we create another method, move the second code block to it then call the new method? Well, that wouldn't really solve anything, as it's just moving code, not reducing it. To run the second Code Block, we make another Method call of the `calculateScore` Method, and pass arguments for the new values.

```java
public class Main {

    public static void main(String[] args) {
	    
	    calculateScore(true, 800, 5, 100);
	    
	    calculateScore(true, 10000, 8, 200);
    }
    
    public static void calculateScore(boolean gameOver, int score, int levelCompleted, int bonus){
	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore); 
	    }
    }
}
```

You've now made another Method call, defined the Arguments and run the second Code Block. Also notice how I've deleted the original Variable definitions and simply passed values as the Arguments rather than the Variable names. You'll also notice that originally, the first Code Block had a fix to increase the Variable `finalScore` which the second didn't, meaning that the calculation for the second Code Block would be wrong. By having a Method do the work, the fix is there, and the two calculations will now be correct.

 You've now reduced two Code Blocks that were 24 lines long, to simply 17 lines, a reduction of 4% (not including white space).

#Returning a Value from a Method:

Another awesome feature of Methods is that it can return a value after its calculation is completed to the method call. This can mean that that value is not lost once the method code is finished, but rather returning the value we want and allows us to use that value later on in the code.

Returning a value is done using the word `void` (or rather the lack of it). When we use the word `void` in the method signature, we're declaring that the method doesn't return a value. If we want our method to return a value, we need to replace `void` with the data type the method will be returning. That can be any of the 8 data types, including strings.

```java
public class Main {

    public static void main(String[] args) {
	    
	    calculateScore(true, 800, 5, 100);
	    
	    calculateScore(true, 10000, 8, 200);
    }
    
    public static int /*step one*/ calculateScore(boolean gameOver, int score, int levelCompleted, int bonus){
	    if(gameOver){
	        int finalScore = score + (levelCompleted * bonus);
	        finalScore += 1000;
            System.out.println("Your final Score was " + finalScore); 
            return finalScore; //step two
	    }
	    return -1; //step three
    }
}
```

I've now adjusted the code so that the menthod returns a value. I changed the `void` to an `int`, which means when the method is finished, it will return a number of type `int` (marked **step one**). I then added a `return` statement at the end of the `if` condition, meaning that once the line "Your final score was " has run, the mehod will return the value of `finalScore`, **Step two**.

If I was to stop there, Java would throw an error. That's because there is an `if` statement. We need to account for what happens if the condition fails (IE: if `gameOver` is false). That is done by **Step Three**, where we say that if the `if` conditional statement returns false and is not run, we return the value of `-1` to the method call, and not the `finalScore` which is only in the conditional statement.

So now we've rturned a value to the method call. This essentially gives the mehtod call (calculateScore()) a value we can use. We can now remove the print statement from the method, and use the method calls value in the print statement back in the `main` method. To do this, you can use the `calculateScore()` method as the value of a variable, then use that variable to output the value of the return:

```java
package com.DominicRoss;
public class Main {

    public static void main(String[] args) {

        int highScore = calculateScore(true, 800, 5, 100);

        System.out.println("Your final score was " + highScore);

       highScore = calculateScore(true, 10000, 8, 200);

       System.out.println("Your final score was " + highScore);
    }

    public static int calculateScore(boolean gameOver, int score, int levelCompleted, int bonus){
        if(gameOver){
            int finalScore = score + (levelCompleted * bonus);
            finalScore += 1000;
            return finalScore;
        }
        return -1;
    }
}
```