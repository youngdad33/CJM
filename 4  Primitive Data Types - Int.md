Variables allow you to store data in memory of the device Java is running on. A Variable can hold all sorts of data from text, numbers, results from operations and even other variables. It's like a box where you want to store something. The Variable is the box, and the Variable name is the lable you put on the box.

Variables can later be recalled to display their data in many ways. First, we're going to talk about the most basic of Variables: The `int`.

## `int` Variable:

The `int` Variable stores whole numbers. `int` is short for *Interger*, a math term for a whole number. To create a `int` Variable, we first use the **[keyword](quiver:///notes/E93E2C95-8E68-44AE-8CFB-C3528DD60BC8)**, then give that variable a name (or, we first make the box, then label it). 

```java
 int myFirstVariable;
```

Here, we've created a Variable (`int`) then given it a name `myFirstVariable`. We next need to add some data to it (add somehting to the box). This is done like this:

```c
int myFirstVariable;
myFirstVariable = 3;
```

Now, if we wanted to call the Variable, we simply use its name.

```java
int myFirstVariable;
myFirstVariable = 3;
System.out.println(myFirstVariable);
```

That's a lot of code for simply expressing a Variable. A quicker way to write that would be to eliminate line 2, and assign a number to the `int` when it's created. This means that you code less *if* you know what the Variable will hold at the time of making it. If not, you can assign it's data later in the program.
To assign data to it at creation, simply add it to the end of line 1:

```java
int myFirstVariable = 3;
System.out.println(myFirstVariable);
```

As mentioned above, Variables can perform calculations too. You could then assign the result to another Variable.

```java
int myFirstVariable = 2;
int mySecondVariable = 3;
int myTotal= myFirstVariable + mySecondVariable;
System.out.println(myTotal);
```

This four line code will not show `2+3=5`, but rather just `5`, because we called the `myTotal` variable which has been assigned the total of the calculation of `myFirstVariable` and `mySecondVariable`.

>You'll note that the Variable Names have been typed in *cammel case*, which is the term given for the first letter of each word in the name being capitalised except for the first. This is standard practice in Java (and most other programming languages) and makes it easier to read the name and therefore your code. An alternative is to use **pipe case**, where you add a `-` between each word of the Variable.

