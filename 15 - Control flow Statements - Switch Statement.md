You've already seen one Control Flow statement in Chapter 12, [If keyword and code blocks.](quiver:///notes/029CE0D2-CFBF-416F-BBE8-CF61FCDCBC19). The `if` keyword allows us to set a condition, and test to see if that condition is true and action certain code depending on if that is true or not. This can be combined with the `else` keyword to test multiple conditions in one Code Block and action any number of code blocks depending on the result.

```java
public static Main {
    public static void Main (String[] args){
        int value = 1;
        if(value == 1){
            System.out.println("Value was 1");
        }else if (value == 2){
            System.out.println("Value was 2");
        }else{
            System.out.println("Value was not 1 or 2");
        }
    }
}
```

The issue with the `if` statement is that it's messy. If there are numerous conditions to test, the `if` statement will go on for ever. There is, fortunately, a handy alternative to test the condition of a statement. This is the Switch Statement.

#The Switch Statement:
The Switch Statement works just the same as the `if` and `else` statement block above, except that the code is a little neater and quicker to type. A simple Switch statement which does the same as the `if` statement above would look like this:

```java
package com.DominicRoss;

public class Main {

    public static void main(String[] args) {
    int switchValue = 1;
    switch (switchValue){
        case 1:
            System.out.println("Value was 1");
            break;

        case 2:
            System.out.println("Value was 2");
            break;
            
        default:
            System.out.println("Value was not 1 or 2");
            break;
    }
    //more code here...
    }
}
```

Here, the `switch` statement is testing the exact same condition as the `if` statement above, but it is much neater and requires less code. I will now explain the individual parts of the statement.

##`switch`:
This is the keyword for the `switch` statement. The condition only needs to be set to the value you are testing. You don't have to add the `==1` as this is decided in the code below.

##`case`:
The keyword `case` is the condition part of the `switch` statement. This is where you test the condition, so on line 8, you're saying *"If value is equal to 1, run this code"*. The code you want to run follows on the next line. Note that `case` must be followed by the value you're testing for and then a colon.

##`break`:
The `break` statement is a very important part of the `switch` statement. It will stop Java from running any further tests and break to the next line of code after the Code Block (in this case, line 20). If you miss out the `break`, you risk running into errors with the code. If your code had 20 cases, and your value was correct on the first case, you will see 20 lines of output which will be all the following cases, or until Java hits a `break` in the  code.

##`default`:
The `default` statement is the final `else` of the `switch` statement. It's essentially saying *"If nothing else is correct, run the following code"*.

##`switch` data types:
The `switch` statement can be used with Byte, Short, Int and Char data types only. As of Java version 7, you can also use the `switch` statement with Strings. Older versions of Java, however, can only use the four data types mentioned earlier.

##`switch` statement shortcut:
I started by saying that if there were a lot of conditions to test, the code would be very long, and with an `if` statement, that's certainly true. but with the `switch` statement, you can have a shortcut to test for any number of conditions, like so:

```java
package com.DominicRoss;

public class Main {

    public static void main(String[] args) {
    int switchValue = 1;
    switch (switchValue){
        case 1:
            System.out.println("Value was 1");
            break;

        case 2:
            System.out.println("Value was 2");
            break;

        case 3:
            System.out.println("Value was 3");

        case 4: case 5: case 6: case 7: case 8: case 9: case 10:
            System.out.println("Value was 4,5,6,7,8,9 or 10");
            break;

            default:
                System.out.println("Invalid input!");
    }
    //more code here...
    }
}
```

In this extended example, not only are we testing to see if the value was equal to 1,2 or 3, but you can also check to see if it was between 4 and 10. By simply adding all the other cases to one line (line 19) and still print a value.