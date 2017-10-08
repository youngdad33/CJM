You may not realise it yet, but you've been using operators since the very first bit of code you typed.

An operator will work on your code and can do one of many things.  
* It can assign an **operand** to a variable.
* It can add, subtract, devide or multiply Variables together.
* It can test to see if statements are true.
* ... and many more.

#The Assignment Operators:
Assignment operators will take the value of the operand and assign it to the variable. 

##The Assignment operator `=`:
You'll recognise the assignment operator, as you've used it in the very first bit of code you typed; [The Hello World App](quiver:///notes/E70F4789-E4C6-485B-9DFE-1EB1D9EA2B5C). Although the Assignment Operator is an equal sign, in coding it means assign the operand to the Variable.

##The Add and assign operator `+=`:
The Add and Assign operator will add the value of the right operand to the left operand and assign the result to the left operand. EG: C += A is the same as C = C + A.

##The Subtract and assign operator `-=`:
Same as above, but subtracts the right from the left then assigns it to the left.

##The Multiply and assign operator `*=`:
Same as above, but multiplies the right from the left then assigns it to the left.

##The Devide and assign operator `/=`:
Same as above, but devides the right from the left then assigns it to the left.

##The Modulus and assign operator `%=`:
Same as above, but modulates the right from the left then assigns it to the left.

#Arithmetic Operators:

Arithmetic Operators are used in mathematical expressions in the same way that they are used in algebra.

##The add operator `+`:
Again, you've seen this operator before when you added `int`'s together and used it for very basic math. The `+` Operator allows you to add numbers together and place them in a variable. It can also be used to add (or concatenate) strings and variables together. In this use, it's not adding variables together in a mathimatical sense, but concatenating them together.

##The subtract operator `-`:
The subtract operator will allow you to perform simple math with variables and take one away from the other.

##The multiply operator `*`:
This operator will allow you to multiply operands or variables containing operands together.

##The devide oeprator `/`:
The devide operator will devide operands or variables from each other.

##The Modulus (or remainder) operator `%`:
The modulus operator will give you the remainder of a devision. If you were to devide 4 by 3, and use the modulus, it would give the answer of 1, as that is how many times 3 can go into 4.

##The Increment operator `++`:
The increment operator is a shortcut for when you want to increase the value of a variable by 1. This is a useful way to save code. Instead of creating a line of code where you call the variable and increase it by one, you can simply use the increment operator to do this:

```java
int hitTarget = 0;
// You hit the target, so increase score by one
hitTarget + 1;
// You hit target again
hitTarget + 1;
```

```java
int hitTarget = 0;
// You hit the target so increase score by one
hitTarget++;
//You hit the target again
hitTarget++;
```

As you can see, the Increment operator allows you to save a little code by increasing the `hitTarget` variable by one.

##The Decrement operator `--`:
Similar to the Increment Operator, but decreases the variable value by one.

#Relational Operators:

Relational Operators are used in **Conditional Statements** and allow you to test if a statement is true or false.

##The Equal To Operator `==`:
The equal to operator will test to see if the values of two operands are equal or not. If they are, then the statement is considered True.

##The Not Equal To Operator `!=`:
The Not Equal To Operator tests to see if the values of two operands are equal or not. If they are not, then the statement is considered True.

##The Greater than operator `>`:
The Greater than operator checks to see if the values of the left operand is greater than the right operand. If it is, then the statement is true.

##The Less Than Operator `<`:
The Less Than Operator checks to see if the value on the left operand is less than the right operand. If it is, then the statement is true.

##The Greater than or equal to operator `>=`:
The Greater than or equal to Operator checks to see if the value of the left operand is greater than or equal to the right operand. If it is, then the statement is true.

##The Less than or equal to Operator `<=`:
The less than or equal to operator checks to see if the value of the left operand is less than or equal to the right operand. if it is, then the statement is true.

#The Logical Operators:

Logical Operators will test to see if a statement is true if both operands are true, if either one is true, or if neither are true.

##The And operator `&&`:
The And operator will test to see if a statements two operands are true. If both are true, then the statement is true. If one or both are false, then the statement is false.

##The Or operator `||`:
The Or operator will test to see if either of the two operands in a statement are true. If either are true, then the statement is true. If both operands are false, then the statement is false.

##The Not Operator `!`:
The Not operator will reverse the logical state of an operand. IE: if it's true, it will change it to false and if it's false it will change it to true.

A full list of the Operators (including some I have not covered yet) can be found [here](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/opsummary.html).

#Operator Precedence:
You must be careful when using operators of their precedence. Operators will take precedence when doing calculations. For example:

```java
int myInt = 40 + 20 * 2
```

You'd expect the anser to be 120. However, because of the precedence of the multiplier, the answer will actually come out as 80. That's because the multiplier takes precedence over the addition, and will times the 20 by 2 before adding the 40. If you want to do the sum in the way we read it, you need to use brackets to make it work:

```java
int myInt = (40 + 20) *2
```

Only this sum will give the answer of 120 because brackets are higher on the table of precedence than multipliers. A list of all the operator precedence can be found [here](http://cs.bilkent.edu.tr/~guvenir/courses/CS101/op_precedence.html).