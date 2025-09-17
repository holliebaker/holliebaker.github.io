# Codelab I Exercises

The best way to learn to code is to... write lots of code. With that in mind, here are some ideas for exercises or projects you can work on.

## Exercises by topic

### Getting started

- <details>
<summary>Hello, world!</summary>

It's a classic. You cannot say you know how to code in a language until you have honoured this [tradition](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program).
Write a program which prints "Hello world!" to your terminal.
</details>

- <details>
<summary>foo, bar and baz</summary>

Write a program which declares three variables, and int, a float and a double, with names `foo`, `bar` and `baz`. Asother rite of passage in programming done. Honourable mention to `pippo`, the lesser-known cousin from Italy. Why not add a `pippo`, type is your choice.

Extra activities:

- What is the largest and the smallest number an `int` can hold?
- How many decimal places can a `float` represent?
- What about a double?
- Read up on floating-point errors.
</details>

- <details>
<summary>Calculate your overall mark</summary>

You have two assessments: S1 is worth 40%, S2 is worth 60%. Write a program which stores the mark for each assessment (which data type should you use?), calculates the total mark, and prints it to the terminal.

Allow the user to enter their marks for S1 and S2 via the terminal.
</details>

- <details>
<summary>Now you've made it personal.</summary>

Write a program which asks the user to input their name, stores it in a variable, and prints out a personalised ~~insult~~ greeting.

Test it. What if the user enters a first and last name?
</details>

- <details>
<summary>Caesar's Cipher, one character at a time.</summary>

The Caesar Cipher (or shift cipher) encrypts a message by "adding" a fixed number, the *encryption key*, to each character in the message.
For example, if the encryption key is `5`, `A` would become `F` (via `B,C,D,E,F`), `G` would become `L`, and `Q` would become `V`. If the end of the alphabet is reached, then wrap back around to the beginning -- e.g., `X` would become `C` (`Y,Z,A,B,C`)

In C++ characters are simply integers in disguise, encoded using the ASCII syste. This means you can "add" numbers to characters. I.e.,
```c++
char c = 'A';
int key = 6;
c = c + key; // c = 'F'
```
You can use the modulo (`%`) operator to handle wrapping around at the end of the alphabet.

Write a program which enciphers one character at a time. I.e., store the character and the key in a variable (start off by hard-coding it, then add user input later, if you like). The program should output the enciphered character to the terminal.

If you know iteration already, then extend the program to encipher a string (if not, don't worry, this will be covered later in the module).
</details>

- <details>
<summary>Fantasy currency</summary>

Let's implement (a cheap rip-off of) a fantasy currency. There are three coins, golden Ships, silver Scythes, and bronze Bolts. It works as follows:

- One golden Ship is worth 17 silver Scythes.
- One silver Scythe is worth 29 bronze Bolts.
- One golden ship is worth 13 Great British Pounds.

Despite the currency being rather complicated, involving additions modulo prime numbers, its inhabitants don't learn maths in school. As a result you have been asked to implement a simple cash register. The shop assistant tells the register how much the purchase costs, drops in the customer's money, and the register spits the correct change back out.

1. Start by working out how to store the currency -- you'll have to perform calculations with it, so bear that in mind.
2. User input: prompt the cashier to enter the transaction amount and the amount of money the user has given.
3. Calculate change: figure out how much change to return, and print this amount out to the terminal -- fantasy customers dislike being given too many coins!
</details>

### Logic and Conditional Statements

<details>
<summary>Users are annoying and we have to deal with it</summary>

Almost every program we write needs to take input from the user. So far, we've assumed that users are sensible, and will give us the values in the format we expect. However, this is seldom the case.

`cin >> someVariable;` attempts to store tha value entered by the user into `someVariable`. If the value cannot be assigned because data types do not match, e.g., if `someVariable` is an `int` but the user entered a `string`, then `cin.fail()` becomes `true`.

Prompt the user to enter a number, and attempt to store it in an `int` variable (or a `float` / `double`, up to you). Use an `if` statement to check the value of `cin.fail()` and print a message to inform the user that they have entered an invalid value.

We'll extend this later to keep prompting the user until they enter a valid value -- you'll find yourself using this code a lot!
</details>

<details>
<summary>Add a pass check</summary>

Return to your mark calculator. In order to pass, you must score at least 40% in both assignments. Add a check to see if the entered marks allow for a pass, if not, print "Fail". Otherwise, calculate the total mark as before.
</details>

<details>
<summary>Insufficient funds check</summary>

Return to your fantasy cash register. What happens if the user does not give enough money to complete the purchase?

Add an insufficient funds check so that the cash register displays a message and returns the user's money if they did not provide enough te complete the purchase.
</details>

<details>
<summary>Types of triangles</summary>

Write a program which decides what type of triangle you have, based on its side lengths. I.e., the user should input three numbers (data type?) and the program should output a message with information about the triangle.

Let $a$, $b$ and $c$ be the side lengths of a triangle, where $c$ is the length of the longest side.
- $a,b,c$ only define a triangle if $a + b > c$.
- If $a = b = c$, then it's an equillateral triangle -- all sides and all angles are equal.
- If two sides have the same length, then it's an Isosceles triangle.
- To check whether it's a right-angled triangle, see if Pythagoras' Theorem works ($a^2 = b^2 + c^2$)
- If it is not a right-angled triangle, figure out whether the largest angle is greater or less than 90 degrees (or $
pi / 2 $ radians, if you prefer).
</details>


