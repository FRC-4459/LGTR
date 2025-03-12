---
title: Java and Object Oriented Programming
tags:
  - "#project/LGTR/programming"
start: 3/11/2025
author: Kingston V.
---
Before starting to program for FRC, you need to grasp the basics (at least) of Java and Object Oriented Programming. This will by no means be a complete guide - a better curriculum can be found on [Codecademy](https://www.codecademy.com/learn/learn-java), [MOOC](https://java-programming.mooc.fi/) (this one is praised a LOT), or [this youtube playlist](https://www.youtube.com/playlist?list=PLE7E8B7F4856C9B19). This document will be a quick, basic layout of the java features you'll need to use for FRC - more of a reference guide then a learning resource. 

If you want to become an FRC programmer, you should either already understand object oriented programming before build season or *teach yourself OOP/Java* wherever you can. There may not be enough resources to dedicate to teaching completely new programmers during preseason. Please try to have a grasp on this stuff before it's time to build.

## Primitive Variables

You can declare a variable, which is a representation of a piece of information, in Java using the syntax `Type Name = Value`. Typically variables are used in FRC programs to encapsulate physical hardware (you'll have to declare a variable for a motor controller or encoder) or commands and subsystems.

Java has eight primitive variable types, some of which are useful for robotics applications. They are as follows:

```java
boolean isFinished = true; // A boolean can be true or false. It represents binary state.
byte b = 4;                // One byte. Don't use this unless you know what you're doing. Ranges between -128 to 127
char letter = 'b';         // One character.
short s = 103;             // A 16 bit signed integer. Ranges between -32,768 and 32,767
int i = 4459;              // A 32 bit signed integer. Ranges between -2,147,483,648 to 2,147,483,647
long l = 445944594459;     // A 64 bit signed integer. Unreasonably broad range. Probably won't overflow.
float f = 103.34;          // A 32 bit decimal number. Single precision. May cause rounding errors.
double d = 103.321321;     // A 64 bit decimal number. Double precision.
```

> [!TIP] Best Practice
> Prefer `double` to `float` wherever possible - it's less susceptible to rounding errors.

If you need to pass simple numbers, a primitive is typically what you'll use. Mostly you'll be passing around doubles.

If you want to change a variable's value, you can do so by using the syntax `Name = Value`.
## Classes

Classes are custom types defined by the user. They act like "blueprints" to create an object. They have two main components - **Fields** (also called members or member variables) and **Methods** (functions). Fields are objects or variables that belong to the class, and they can be of any type, including other classes. Methods are blocks of code that do work relating to the class.

Fields are defined like any variable, except with an access specifier before: `Access Type Name = Value`. The access specifier is either "public" or "private". Public fields can be accessed from anywhere else in code, whereas private fields can only be accessed within the class. You should try to make as many fields private as possible, because poor access from elsewhere in the code can modify your variables in ways you don't expect. Whenever you want to change or access your fields, you should write a getter or setter to give some guardrails to that behavior.

Methods are pieces of code that take objects and run operations on them. You can declare a method with the syntax `Access ReturnType Name(Type Parameter1, Type Parameter2) { code; }`. The parameters are objects that the user can pass into the function which may change how the function works. To use a function, call it with the syntax `Object.method(param1, param2);`.

All classes also have a constructor. A constructor is a method with the same name as the class, which returns a new object made from the class.

```java
public class Car {
	private int cost;              // Fields typically shouldn't have a default value.
	private boolean locked = true; // Unless you *need* the field to start with one.
	private Motor motor;           // This field will hold a Motor object.
	private int wheelSize;

	public Car(int cost, Motor motor, int wheelSize) {
		this.cost = cost;          // Use this.{field} to specifically reference a field on the object you're in.
		this.motor = motor;
		this.wheelSize = wheelSize;
		/* At this point, the fields all hold a value that the user passed in to the constructor. */
	}

	public int getCost() {         // Non-constructor methods need return values; if you don't return anything, set this to 'void'.
		return this.cost;
	}

	public void setCost(int newCost) {
		this.cost = newCost;
	}

	public double getDriveDistance(double time) {
		double totalDistance = time * horsepower;
		return totalDistance;
	}
}
```
## Objects

Objects are variables that aren't primitive, but rather constructed from a class. You can't directly call the methods or access the fields on a class (unless it's static, but that's another topic) until you make an object out of it. You can access fields and call methods of an object using a period. Here is an example using the previous class:

```java
import myProject.Car;                        // The class belongs in a different file; import it to use it.
import com.Cummins.Engine;                   // Someone else made the Engine object; import it from a library.

public class Example {
	public static void main(String[] args) { // main() is the entry point for a Java program.
		Engine v8 = new Engine(8);
		Car my_whip = new Car(37000, v8, 6); // $37000 car with a v8 engine and 6 inch wheels.
		
		double two_minute_distance = my_whip.getDriveDistance(120);
	}
}
```

## Lists

Lists are objects that contain an assortment of other objects. Lists are very useful when you have pieces of related or sequential data and you don't know how many variables you'll need for them - or there are too many to reasonably write out variables. There are a variety of list/collection objects in Java and every other programming languages, but most often you'll be using the ArrayList. ArrayLists are lists that are dynamically sized - they can shrink and grow on demand to fit your objects.

List objects almost universally implement *indexing* as a way to access the elements in the list. Each element is given a sequential index - the first element is 0, the second element is 1, and so on. To access an element from the list, use the syntax `list[index]`.

```java
import java.util.ArrayList;                                    // Most standard library objects have to be imported from java.*

public class Example {
	public static void main(String[] args) {
		ArrayList<int> my_list = new ArrayList<int> (1, 2, 3); // The list state looks like: { 1, 2, 3 }
		int num = my_list[1];                                  // num contains the number 2.
		my_list[2] = 10;                                       // The list state looks like: { 1, 2, 10 }
		my_list.add(4459);                                     // The list state looks like: { 1, 2, 10, 4459 }
	}
}
```

## Boolean Expressions

A boolean expression is any combination of objects, variables, and operators that results in a "true" or "false" value. Boolean expressions are an incredibly important part of writing code in modern languages, and also a big potential source of bugs. It's worth it to pay extra attention to these expressions. Every boolean expression consists of a boolean or comparison operator and some values.

```java
public class Example {
	public static void main(String[] args) {
	/* Both types of operators require a value on the left and right to evaluate. */

	/* Boolean operators */
	&& // AND Returns true if values on the left and right are true
	|| // OR Returns true if one of the values, left or right, are true
	^  // XOR returns true if only one of the values are true
	!  // NOT flips a value from true to false or false to true

	/* Comparison Operators */
	== // Returns true if the values on left and right are equal. DO NOT USE FOR OBJECTS.
	!= // Returns true if the values on left and right are not equal. DO NOT USE FOR OBJECTS.
	>  // Returns true if the value on the left is greater than the one on the right.
	<  // Returns true if the value on the right is greater than the one on the left.
	>= // Returns true if the value on the left is greater than or equal to the one on the right.
	<= // Returns true if the value on the left is less than or equal to the one on the right.
	}
}
```

Objects should not use direct comparison operators. Instead, objects that may need to be compared generally implement a `.equals()` method. This should be used instead - direct comparisons between objects using double equals signs will almost always return false even if the objects are functionally equal for reasons beyond the scope of this guide.  

Here is an example for use of each operator:

```java
public class Example {
	public static void main(String[] args) {
		boolean is_raining = true;
		int temperature = 82;
		boolean is_cold = temperature < 70;

		boolean wear_heavy_coat = (is_raining && is_cold);   // false
		boolean wear_long_sleeves = (is_raining || is_cold); // true
		boolean cold_or_raining = (is_raining ^ is_cold);    // true
		boolean sunny_day = (!is_raining)                    // false

		boolean is_seventy = (temperature == 70);            // false
		boolean isnt_seventy = (temperature != 70);          // true
		boolean over_seventy = (temperature > 70);           // true
		boolean under_seventy = (temperature < 70);          // false
		boolean deadly_heat = (temperature >= 104);          // false
		boolean ice_freezes = (temperature <= 32)            // false
	}
}
```

## Conditional Flow

Conditionals are the primary use of boolean expressions, and the way to create code that does different things at different times. Conditional flow consists of `if` blocks, `else if` blocks, and `else` blocks primarily.

`if` blocks use the syntax `if (condition) {code}` and are the most basic conditional block. The condition in the parenthesis must evaluate to a boolean - i.e., be a boolean expression - and as long as the condition evaluates to true, the code in the block will run, and **no more `if` or `else if` blocks in the sequence will be allowed to run.**. If the condition evaluates to false, the code will be skipped over and program execution will continue.

`else if` blocks use the syntax `else if (condition) {code}` and can only be placed after an `if` block. If the conditional in the first `if` block evaluates to `false`, the `else if` will run its conditional the same way the `if` block did. If the expression in `conditional` evaluates to true, the `else if` block will be allowed to run and **no more `if` or `else if` blocks in the sequence will be allowed to run.** If the expression in `conditional` evaluates to false, the `else if` block will be skipped over.

`else` blocks use the syntax `else {code}`. `else` blocks run at the end of an `if`/`else if` chain **if none of the previous blocks' conditionals evaluated to true**. The `else` block is a way to tell the program "run this code in any situation my conditionals didn't already account for". The `else` block must be at the end of the `if` chain, and there can only be one per chain.


```java
import myProject.clothes.Top;
import myProject.clothes.Wardrobe;

public class Example {
	public static void main(String[] args) {
		int temperature = 42;
		Wardrobe closet = new Wardrobe();
		Top my_top;                   // We don't know which top we'll wear, so don't give this object a value yet

		if (temperature < 50) {       // Catches any temperature under 50
			my_top = closet.getCoat();
		}
		else if (temperature <= 60) { // Catches any temperature between 50 and 60, inclusive
			my_top = closet.getJacket();
		}
		else if (temperature <= 70) { // Catches any temperature between 61 and 70, inclusive
			my_top = closet.getLongSleeve();
		}
		else {                        // Catches any other temperature
			my_top = closet.getShortSleeve();
		}
	}
}
```

## Loops

Loops are the primary way to repeat code many times in your program. Most often, this is used to iterate over all the objects in a list or to program a system that stays on for an extended period of time. There are two types of loops in Java: `for` loops and `while` loops.

`for` loops use the syntax `for (counter; comparison; step) {code}`. `for` loops are intimidating and tricky at first but the core concept is simple. Firstly, the for loop creates a new variable in the `counter` section. Typically this is just an integer initialized to zero - so this looks like  `for (int i = 0; comparison; step) {code}`. Then, the `for` loop runs the expression in the `comparison` section. Typically, this is a "less than" comparison, but it can be anything. If the `comparison` evaluates to `true`, the loop will run once; if it evaluates to `false`, the loop will stop running and the code will continue executing after the loop. By this point, or loop may look like `for (int i = 0; i < 10; step) {code}`. This loop will compile and run, but without a `step` block, `i` will stay at zero forever and the `comparison` will always be true. This will send your program into an infinite loop, stopping code execution!

> [!WARNING]
> If your program stops executing but does not throw an exception or crash, and there is no console or robot output, you may be in an infinite loop! Check your conditionals to make sure that they must eventually become false.

To fix this, the `step` block is run once each time the `for` block's `code` finishes executing. Anything written into the `step` block should compile, but typically the statement there modified your `counter` in some way. An example step looks like this: `for (int i = 0; i < 10; i++) {code}`, where `i++` increases `i` by one. This loop will now run 10 times and stop after the 10th.

Here is a flowchart explaining for loop control flow:
![[1679044531720-1-01 (13).png]]

And here are two examples of for loops being used:

```java
public class Example {
	public static void main(String[] args) {
		int count = 0;

		for (int i = 0; i < 99; i++) {
			count++;
		}

		/* At this point, 'count' is 99. */

		int second_count = 0;
		
		for (int i = 200; i > count; i--) { // 'i' can be created again because it's destroyed after the first for loop ends.
			second_count++;
		} 

		/* At this point, 'second_count' is 101. */
	}
}
```

There is a second type of `for` loop, called a *range-based for loop*. This is a simpler type of loop designed to easily iterate over a collection. Range-based `for` syntax looks like this: `for (Type Name: Collection) {code}`. On the first loop, the `for` loop will attempt to assign the first element of `Collection` to the object `Name`. On the second loop, it will attempt to assign the second element of `Collection` to `Name`, and so on until every object has been iterated over.

```java
import java.util.ArrayList;

public class Example {
	public static void main(String[] args) {
		int count = 0;
		ArrayList<int> list = new ArrayList<int> (1, 4, 2, 6);

		for (int num : list) {
			count = count + num; // On the first loop, count is 1; on the second, it is 4; and so on.
		}

		/* At this point, count is 13. */
	}
}
```


> [!TIP] Best Practice
> Unless you need to do math with the index, you should prefer range-based for loops when iterating over collections.

Finally, `while` loops are the simplest type of loop. The syntax looks like this: `while (condition) {code}`. It's as simple as it looks: before every loop, the `while` will evaluate `condition`. If the `condition` is true, it will run once more; if the `condition` is false, it will stop running and continue execution after the loop. `while` loops are typically reserved for niche use cases where the structure of a `for` loop is too limiting. While you may sometimes need to write a `while` loop, understand that it's much easier to create bugs and infinite loops when handling iteration yourself.

> [!TIP] Best Practice
> Prefer `for` loops over `while` loops wherever possible.

```java
import com.robotics.Robot;

public class Example {
	public static void main(String[] args) {
		Robot my_robot = new Robot();
		int distance_to_wall = my_robot.getFrontSensorDist();

		while (distance_to_wall < 10) {
			my_robot.driveForward();
			distance_to_wall = my_robot.getFrontSensorDist();
		}

		/* At this point, the robot should be roughly 10 units from the wall. */
	}
}
```


## Next Steps

Congrats! You know the basics of Java programming. This is 95% of what you'll need to program FRC robots - but there is still some use of advanced concepts like polymorphism and inheritance, lambda functions, and event loops. These topics are worth researching yourself but they will also get brief explanations in their relevant sections in the [[Command Based Programming]] article.

If you believe you already have a solid grasp of the fundamentals of programming in Java, you can skip straight to [[WPILib]] - if not, I'd encourage you to build the [[Project - Vending Machine Simulation]] before moving on.