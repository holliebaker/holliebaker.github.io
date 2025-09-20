---
layout: codelab
---

## Getting Started

### Hello, world!

It's a classic. You cannot claim to be able to code in a language until you have honoured this [tradition](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program).
Write a program which prints "Hello world!" to your terminal.

Commit your work and push it to GitHub (you can use the `codelab-i` repo, or create a now one to store your projects).

### Foo, Bar and Baz

Write a program which declares three variables, and int, a float and a double, with names `foo`, `bar` and `baz`. Another rite of passage in programming done. Honourable mention to `pippo`, the lesser-known cousin from Italy. Why not add a `pippo`, type is your choice.

<details markdown="block">
<summary>Extension tasks</summary>

- What is the largest and the smallest number an `int` can hold?
- How many decimal places can a `float` represent?
- What about a double?
- Read up on floating-point errors.

</details>

Don't forget to commit your work and push it to GitHub.

### Mark Calculator

You have two assessments: S1 is worth 40%, S2 is worth 60%. Write a program which stores the mark for each assessment (which data type should you use?), calculates the total mark, and prints it to the terminal.

Allow the user to enter their marks for S1 and S2 via the terminal.

### Now you've made it personal

Write a program which asks the user to input their name, stores it in a variable, and prints out a personalised ~~insult~~ greeting.

<details markdown="block">
<summary>Extension task</summary>

Test it. What if the user enters a first and last name?

</details>

### Caesar's Cipher, one character at a time

The Caesar Cipher (or shift cipher) encrypts a message by "adding" a fixed number, the *encryption key*, to each character in the message.
For example, if the encryption key is `5`, `A` would become `F` (via `B,C,D,E,F`), `G` would become `L`, and `Q` would become `V`. If the end of the alphabet is reached, then wrap back around to the beginning -- e.g., `X` would become `C` (`Y,Z,A,B,C`)

In C++, characters are simply integers in disguise, encoded using the ASCII syste. This means you can "add" numbers to characters. I.e.,
```c++
char c = 'A';
int key = 6;
c = c + key; // c = 'F'
```
You can use the modulo (`%`) operator to handle wrapping around at the end of the alphabet.

### Old skool cash register

Let's build a cash register which deals with [pre-decimal currency](https://en.wikipedia.org/wiki/Coins_of_the_pound_sterling#Pre-decimal_coinage) (pounds, shillings and pence).

- £1 = 20 shillings (20s).
- 1 shilling = 12 pence (12d).

The cash register should work as follows: the cashier will enter the value of the transaction (in pounds, shillings and pence) and drop in the customer's money. The cash register should calculate the customer's change and return it to the cashier for them to hand over1.

1. Start by working out how to store the currency – you’ll have to perform calculations with it, so bear that in mind.
1. User input: prompt the cashier to enter the transaction amount and the amount of money the user has given.
3. Calculate change: figure out how much change to return, and print this amount out to the terminal – fantasy customers dislike being given too many coins!

<details markdown="block">
<summary>Extension task</summary>

Modify your cash register to work with coins. I.e., calculate the coins needed for the given change.
The following coins were used:

- Crown = 5 shillings
- Half crown = 2 shillings and 6 pence
- Florin = 2 shillings
- Shilling = 1 shilling
- Sixpence = 6 pence
- Threepence = 3 pence
- Penny = 1 pence

For example, change of 1 shilling and 10 pence could be given as a one shilling coin plus ten pennies, but nobody likes having a pocket full of shrapnel, so it would be better to give the customer one shilling, one sixpence, one threepence and a penny.

</details>

Tip: after you've got each step working, commit and push your work. Then you can easily return to an earlier working version, if you need to.

