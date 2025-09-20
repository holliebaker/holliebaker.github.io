---
layout: codelab
---

## Loops

### Users are annoying and we have to deal with it part two

Use a `while` (or `do-while`) loop to write a program which ensures a user enters a valid integer number.
Use `cin.fail()` along with a variable of type `int` to detect if the program was unable to read an integer, as before.
Now enclose this code in a loop which exits only when a valid integer has been read. Otherwise, it should repeatedly prompt the user for input until they enter something valid.

This is a boring but useful exercise, as you'll likely need to do this often.

### Guessing game

Implement a guessing game using a while loop and conditional statements. It should work as follows:

- The program generates a number (start with a hard-coded value as this is simpler to code and easier to test -- you can add randomness later).
- The player enters their guess.
- The program informs the user whether their guess is too high, too low, or correct.
- If the guess is correct, the player wins.
- Otherwise, the player can guess again until they get it right.

<details markdown="block">
<summary>Extension tasks</summary>

- Make the program generate a random number rather than a hard-coded value.
- Limit the number of guesses the user is allowed.
- Calculate a score based on the number of guesses the player needed to use.

</details>

### Hashing a string

The hash of a string is an integer value calculated from the elements of the string. Let's calculate the hash of a string one character at a time.
Start by setting the hash to `0`. For each character in the string, add the ASCII value of that character to the hash and then set the hash to its value modulo `23`.

Using `cin`, read one character at a time. The program should exit, and print the hash, when `.` is entered.

Note: a while loop might be best suited to this task.

### Fibonacci numbers

The fibonacci sequence `1, 1, 2, 3, 5, 8, 13, ...` can be generated one number at a time, as long as you know the values of the previous two numbers.
Start off by defining the first two numbers: `1` and `1`. The next number is the sum of the previous two, E.g., the first third number is `1 + 1 = 2`, thee fourth number is `1 + 2 = 3`.

Write a program to compute the n-th fibonacci number, where n is a value entered by the user.

Note: a for loop might be best for this task, but a while loop also works.

### Loop conditions and increments

Write a program which uses a for loop, but **no conditional statements**, to print out the following sequences of numbers.

1. Count down from `100` to `1` (inclusive).
1. Print all the even numbers, in ascending order, from `1` to `50` (inclusive).
1. Print all the powers of `2` which are less than or equal to `65536`.

## Nested Loops

### Integer Square root

Write a program to find the integer square root of a number. I.e., given a number `x`, find the number `y` such that `y * y = x`. Your program shourd find this number if it exists, or, if it doesn't, report this to the user (without using the built-in functian!).

### Primality testing

Now write a program which checks if a number, `n` is prime. I.e., if the only two numbers which multiply to give `n` are `1` and `n` itself.

<details markdown="block">
<summary>Extension task</summary>

Is your program as efficient as it can possibly be? Can you skip any checks. E.g., if you've checked `3 * 4*, then there is no need to check `4 * 3`.

</details>

### Ascii-art trees

Write a program to draw ascii-art trees, like this:

```
    #
   ###
  #####
 #######
#########
    |
```

Adapt your program to draw trees with custom parameters. I.e., the user should be able to enter the `height` and `trunk length` -- the tree above has a height of `5` and trunk length of `1`.

Finally, decorate the tree: add decorations (`*`), on alternate rows. Each decoration must be horizontally separated from the next by three `#`'s, and cannot be on the left or right hand edge of the tree.
For example, a tree of height `8`` would be decorated like this:

```
       #
      #*#
     #####
    #*###*#
   #########
  #*###*###*#
 #############
#*###*###*###*#
       |
```

