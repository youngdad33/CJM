Now we come on to two very special Variables, the `char` and the `boolean`. I say special because they each have a very special function, almost singular in their use.

##The `char`:

The `char` is short for Character, and, as the name suggests, it can hold only **one** character. It has a memory width of **16 bits (2 bytes)**.  It may seem pointless to have a Variable that can hold only one character, but that character can be anything, from a letter (either upper case or lower case), a number (singular only) or a special symbol (like £).  The `char`'s most comon use, however, is for a Unicode Character.

A Unicode Character is a special symbol that isn't usually shown on a keyboard and requires a set number of keys to display it. Fortunately, these are standardised worldwide. The use of a `char` as a Unicode Character Variable (and the reason it is 2 Bytes wide) is because the key combination is longer than one character. For that reason, and escape character is needed to use a Unicode Character with the `char`.

> A table of the Unicode Characters can be found at [unicode-table.com](https://unicode-table.com/en/#control-character).

Let me show you how a Unicode Character can be used with the escape key in a `char`:

```java
// Width of 16 bits (2 bytes)
char myChar = '\u00AE'
System.out.println("Unicode Character is: " + myChar)
```

The following code will output the following to the Command Line:

![Screen Shot 2017-07-18 at 23.03.15.png](resources/391FF705B551DF3065FBBF2EA28517AE.png =267x83)

It's very important that the escape character, `\u` is added before the code for the Unicode Character. If not, the compiler and the IDE will throw up an error because there is more than one Character in the `char`.

## The `boolean`:

A `boolean` is a Variable that can have only one of two assignments: `true` of `false`. **Nothing** else can be used in a `boolean`.

`boolean`'s are used for conditional statements like `if`, `or` and `while`. Since you don't know about these yet, I will leave this for the moment till we come on to Conditional Statements. Suffice to say that to create a `boolean`, you simply use the keyword `boolean`.