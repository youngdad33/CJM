#`if` statements:
The `if` statement we have seen before. It evaluates an expression to see if it is true, then completes the code within the code block. Now, I'm going to elaborate more on the `if` statement.

##Simple `if` statement:
A simple `if` statement will evaluate one expression, and run one piece of code depending on that evaluation.

```java
boolean gameOver = true;
int myScore = 10000;

if(gameOver == true){
    System.out.println("Your score was " + myScore)
}
```

The `if` statement is line 4-6 and evaluates if the `int` gameOver is true, then runs the statement if it is.

##Complex `if` statements:
Simple enough. But you can expand on the `if` statement by adding a `else` statement.

```java
// using same variables as above.
int livesLeft = 5;
if(gameOver == true && livesLeft = 0){
    System.out.println("Your score was " + myScore)
} else if(gameOver == false && livesLeft > 0) {
    System.out.println("You still have " + livesLeft " lives left, continue?")
}
```

Here, I've added an `else` statement which will only run if the first condition evaluates to false. In this case, because lives left is greater than 0, the only code printed will be that in the `else if` statement stating that you still have more lives left and can continue.

`if` and `else` statements can be chained together to test for numerous conditions and run a statement based on the outcome. Java will only run the first statement it finds to evaluate to true, then break out of the loop and move on to the code below.

It is worth noting, that if the `if` statement only has one statement in its code block, you can code it without the braces. Java will know that this statement is to do with the `if` statement and run it if the condition is true. Otherwise, it will ignore it. But, if the conditional statement has more than one statement in the block, the braces `{}` must be used! In reality, it's best to use the braces anyway, as it makes your code easier to read.

One more note about `if` statements. Rather than writing the conditional expression as `if(gameOver == true)`, you can miss out the `== true` and simply put `if(gameOver)`. This is the same as writing the `== true`, but saves you the code, and makes it neater.

#Code Blocks:
Code blocks is any code within the braces. This belongs to the parent statement and will only run if called upon (if the conditional statement is true, for example).

It's important to know that Variables can be used from outside the code block, and that variables can be created inside the code block. However, variables created within the code block **cannot** be used outside it.

```java
// Using same code example as above.
int levelCompleted = 5;
int bonus = 1000;

if(gameOver){
            int finalScore = myScore + (levelCompleted * bonus);
            System.out.println("Your Final Score was " + finalScore);
        }
finalScore++
```

In this example, the variable `finalScore` was created and defined within the code block. We will not be able to use that variable after the code block (the last `}`) because once that code block is finished, Java deletes the variable from its memory as it's no longer usable. So the code on line 9 will throw an error, because Java will say it hasn't been assigned (outside of the code block).

This phenomenon is called code Scope. A variable's scope is very important, and will be looked into in later lessons.

A major issue with Code Blocks is that there is no way of reusing the code without overwriting the values. You can reuse the variables in multiple code blocks, but to do so, you have to delete their previous values, meaning if you wanted to save them for later on, you can't. The other issue is that to do the same calculation multiple times, you need to retype the code multiple times (the code block from line 5-8). This makes very messy code, and can make your code unnecessarily long. Finally, if you change the code in one code block, you need to change it in all the repeated code blocks to give all the results the same calculations. If you've repepated it a dozen times, that could be a lot of recoding needed.

The solution for this is using a method, and that allows you to re-use code without deleting the previous values. This will be talked about in another lesson.