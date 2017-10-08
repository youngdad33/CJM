You saw in [16 - Control Flow Statements - For Statement:](quiver:///notes/2E1E9A3F-7E55-42EE-93EA-018F362B81FD) how you can use the `for` loop to run code a set amount of times before it exits (or breaks). But what if you don't know ahead of time how many times you need to loop? That's where the `while` loop comes in.

##The `while` Loop:
In a `while` loop, you don't initialise a parameter in the loop, because you don't know how many times it needs to be looped for. Therefore, it has to be initialised outside.

```java
public static void main(Sting[] args){
    int count = 1;
    while (count != 6){
        System.out.println("Count value is " + count);
        count ++
    }
}
```

In this simple `while` loop, you're looping up until the value of `count` is equal to 5. For comparison, the same result would be achieved in the following `for` loop:

```java
public static void main(Sting[] args){
    for (int i = 1; i <7; i++){
        System.out.println("Count value is " + count);
    }
}
```

Although the `for` loop is fewer lines, you know exactly how many times we're going to loop for. The `while` loop is used for occasions when you don't know how many times exactly you will need to loop.

Another - and more common - way of writing the above code is to use a `while true` loop.

```java
public static void main(Sting[] args){
    int count = 1;
    while (true){
        if (count == 6){
            break;
        }
        System.out.println("Count value is " + count);
    }
}
```

This method of writing the code is more popular in Java, and therefore I have added it here for familiarisation purposes.

>REMEMBER: there are to gotcha's with this type of statement: One, you must remember not to fall into an infinite loop (as dicussed in [16 - Control Flow Statements - For Statement:](quiver:///notes/2E1E9A3F-7E55-42EE-93EA-018F362B81FD)) and Two, remember that if your initial value is greater than the test parameter, the loop will not be used at all.

##The `do wile` loop:
The `do while` loop is an addition to the `while` loop. It uses exactly the same rules as the `while` loop, but will always run at leas once before stopping. To run the same code again in a `do while` loop, you write the following code.

```java
public static void main(Sting[] args){
    int count = 1;
    do {
        System.out.println("Count value was " + count);
        count ++
    }while(count != 6);
}
```

This method of writing the code will ensure that the loop is run at least once no matter what the value of `count` is. The new gotcha with this is that if the value of count is the same as the test, you will get stuck in an infinite loop again, because by the time the `while` statment is evaluated, the count will no longer be equal to 6 because you've just increased the count. A clever way of preventing this is by using the `break` command so that you can stop being looped infinitely.

```java
public static void main(Sting[] args){
    int count = 1;
    do {
        System.out.println("Count value was " + count);
        count ++
        if(count <100){
            break;
        }
        }
    }while(count != 6);
}
```

##The `continue` Keyword:
A new keyword you won't have met yet is called the `continue` keyword. It is similar to the `break` keyword in that it gets you out of a loop, but rather than starting on the next line after the loop, you start back at the begining of the loop and test the next conditional statment.

```java
while (number >= lastNumber){
    if(!isEvenNumber(number)) {
        number++;
        continue;
    }

    System.out.println("Even number " + number;)
    number++;
    totalEvenFound++;
}
// More code...
```

In this example of the `while` loop, you're testing to see if a number is an even number or not. If it is, then the second loop is run; you print it to the console, increase `number` then indrease `totalEvenNumber`. If the number isn't even, then the first block is run on line 2. Here, it tests to see if it is not even. It will then increase the number, and come to `continue`. Instead of exiting the `while` loop completely and moving to line 11, we return to line 1 to test the parameters. If they are false, then we continue. If the are true, then AND ONLY THEN do we move on to line 11.
So the `continue` keyword is useful to break out of a loop but still want to continue with the rest of it's function. If you've completely finished with the loop, you would use the `break` keyword.