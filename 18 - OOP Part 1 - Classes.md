Object Orientated Programming is the main advantage of Java. I talked about how being an Object Orientated Programming (OOP) Language was one of Java's stregths. Java is not the only OOP available, but it is one of the most common. But what is an Object?

#Objects:
If you look around you, you can see many examples of Objects: this computer, your watch, your glasses, the bed... These are all objects. All Objects have a state. In the case of the computer, that can be on or off, but it can also determine what RAM it has, the OS it's running, the size of the SDD, the speed of the CPU, etc. The bed can be made or unmade, full or empty.
All these objects also have a behaviour. A behaviour is something the object is doing EG: making a sound, booting up, shutting down, ringing, making a sound, printing, etc.

Software objects mirror these states and behaviours too. States are defined by `fields` (AKA variables). Behaviours are defined by `methods`. You've leant about these two constructs already. An object is defined by a class.

#Classes:
A class has been likened to a blueprint or template for creating an object in OOP. You make a object by creating a class.

You may not realise, but you've been using a class since lesson one; the `Main` class is a class which runs the program. Just like the `main` Method is the beginning method of your program, so the `Main` class is the beginning Class for your program. That doesn't mean you have to put all your code in them. Just as you can create multiple methods, you can have multiple classes. Remember, everything in your program runs through the Main.

Classes aren't just code writen on the screen. They are individual files that have to be compiled by Java to run. When you create a class, you're also creating a brand new file in the package directory.

![Screen Shot 2017-09-30 at 00.08.44.png](resources/6D752710F9D9704AB7270268BA786C36.png =1238x174)
*18.1: Screenshot of Main class shown in project viewer and finder*

![Screen Shot 2017-09-30 at 00.12.32.png](resources/EE73B950FA6CB62F295C5AC662549C68.png =852x169)
_18.2: Screenshot of Main class and new Car class in project viewer and finder_

You can see in 18.1 that the `Main` class is showin in the project viewer in IntelliJ and the corresponding file in the Finder. 18.2 shows the same when you create a new class called `Car`. This is achieved by right clicking on the package folder in IntelliJ, selecting New, then Class (the alternative is to create a new text file with the class name and the `.java` extension).

##Why bother with classes?
The main question you could be asking is why bother making lots of different classes for everything? Why not just use methods to create what you want. The very (**very**) simple answer is that classes are powerful ways of writing code.

So far, we've been using very primitive data types (`int`, `short`, `long`, etc). Think of a class as a powerful user-defined data type. It's not rigidly set by Java, and can hold any data you want. A primitive data type couldn't do that.
> Think of the class as a primitive data type on steroids. *Tim*