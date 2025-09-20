---
layout: codelab
---

## Logic and Conditional Statements

### Users are annoying and we have to deal with it

Almost every program we write needs to take input from the user. So far, we've assumed that users are sensible, and will give us the values in the format we expect. However, this is seldom the case.

`cin >> someVariable;` attempts to store tha value entered by the user into `someVariable`. If the value cannot be assigned because data types do not match, e.g., if `someVariable` is an `int` but the user entered a `string`, then `cin.fail()` becomes `true`.

Prompt the user to enter a number, and attempt to store it in an `int` variable (or a `float` / `double`, up to you). Use an `if` statement to check the value of `cin.fail()` and print a message to inform the user that they have entered an invalid value.

We'll extend this later to keep prompting the user until they enter a valid value -- you'll find yourself using this code a lot!

### Add a pass check to your overall mark calculator

Return to your mark calculator.
In order to pass the module, you must score at least 40% in both assignments. Add a check to see if the entered marks allow for a pass, if not, print "Fail". Otherwise, calculate the total mark as before.

### Insufficient funds check

Return to your pre-decimal cash register. What happens if the user does not give enough money to complete the purchase?

Add an insufficient funds check so that the cash register displays a message and returns the user's money if they did not provide enough te complete the purchase.

### Triangle classifier

A triangle can be defined by the lengths of its sides: A, B, and C.

Write a program which decides what type of triangle you have, based on its side lengths.
The user will input three numbers, representing A, B and C.
The program then outputs which [type of triangle][https://en.wikipedia.org/wiki/Triangle#Definition,_terminology,_and_types] is defined by A, B, C.

You can assume that the sides are entered in ascending order, i.e., C is the longest side and A is the shortest side.
It should identify the following types of triangles.

- Not a triangle: if A + B <= C.
- Equillateral: if all sides have the same length.
- Isosceles: if two of the sides have the same length.
- Right-angled: you can check this using pythagoras' Theorem. I.e., if A^2 + B^2 = C^2 then it's a right-angled triangle, otherwise it is not.

<details markdown="block">
<summary>Extension task</summary>

Adapt your program to handle the case when the numbers are not entered in ascending order.
I.e., for your existing logic to keep working, you'll need to re-arrange the inputted numbers so that A <= B <= C

</details>

### Days in each month

Write a program which takes a number from 1 to 12 as input, representing a month of the year.
The program should use a **switch statement** to output the number of days in that month.

<details markdown="block">
<summary>Extension tasks</summary>

- What happens if the user enters a number which doesn't represent a month of the year.
- What happens if the user enters some input which is not a number?
- What about leap-years?

</details>

### Terminal User Interface

Use a **switch statement** to create a Terminal User Interface.
The user should be able to enter a number, or letter, corresponding to a menu choice.
Don't forget to consider input validation.

### Calculator App

Use a switch statement to build a terminal-based calculator. The user should be able to enter a number, an operator and a second number. E.g., `3 + 5`.
Process this input, storing the two numbers and the operator in variables, then use the switch statement to decide which mathematical operation to perform.

### Roman Numerals

Use a **switch statement** to convert roman numerals `I, II, III, IV, V, VI, VII, VIII, IV, X` into their numerical counterparts.
Can you use *fallthrough* to make your code, if not simpler, but shorter?



