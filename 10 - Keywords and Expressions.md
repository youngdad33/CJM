#Keywords:
Keywords are names of special functions being used by Java and who's name is reserved. There are 53 reserved keywords in Java, many of which you have already seen up till now.

##Example of Keywords:
* `double`
* `float`
* `int`
* `long`

These four keywords you've already used in the code in previous notes. You must know that Keywords cannot be use as variable names, as they will throw an error in the code. You can use them alongside other characters as a variable name, but not exactly as they would be in the code.

```java
int int = 4;
// This is invalid code, as the variable name is exactly the same as the keyword.
int int2 = 4;
// This is valid code, as the variable name is slightly different to the keyword.
```

Using a keyword as a variable name is not a good idea anyway, as it could make you code harder to read. Best come up with your own variable names which link to the variable itself like `highScore`, `boatLength` or `exactDate`.

A full list of the 53 keywords can be found [here](https://en.wikipedia.org/wiki/List_of_Java_keywords).

#Expressions:
An expression in coding is the peice of code that defines a variable, does some work or declares something. Expressions are made up of operators, names and values.

```java
int myInt = 4;
```

In the code example above, the expression is made up of `myInt = 4`. Here, we have the Variable (`myInt`) the operator (`=`) and the value (`4`). The other code on the line (`int` and `;`) does not form part of the expression (but does form part of the statement).

```java
if (myInt == 4){
    System.out.println("myInt is equal to " + myInt)
}
```

This block of code has two expressions in it. Firstly, on line one, the `myInt == 4` inside the brackets is an expression. Secondly, on line two, the `"myInt is equal to " + myint` is the second expression.