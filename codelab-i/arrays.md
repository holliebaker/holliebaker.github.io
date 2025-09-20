---
layout: codelab
---

## Arrays

### Search and Sort

1. Start by defining an array containing 10 numbers.
1. Use a for loop to determine whether the array contains `42` (or a number of your choice, or a value entered by the user).
1. Now check whether the array is sorted in ascending order. I.e., check whether the current element is greater than or equal to the previous one.
1. Sort the array by comparing and swapping elements (figure out a method of sorting yourself, or do some research into sorting algorithms -- you may want to compare your solution with a friend, to see who can sort their array in the fewest steps).

### Version Codename Generator

There is a famous Linux distro whose codenames consist of an animal and an adjective. Write a program to generate version codenames.

1. Start by declaring two arrays, one should contain animals and the other adjectives.
1. First, output all the possible codenames: loop through the animals and, for each animal, loop through all the adjectives, printing each combination.
1. Now refine your solution: valid codenames are those where the animal and adjective both start with the same letter. Allow the user te enter the starting letter and output only the codenames corresponding to that letter.
1. Can you use a similar set-up, with two arrays, to tell knock-knock jokes?

## See also

- [Ciphers](./ciphers)

## Two-dimensional Arrays

### Simple counting

1. Create a `10` by `10` 2d array.
1. Fill it with the numbers from `1` to `100` in ascending order.
1. Print out the numbers in a grid.

### Minesweeper

Implement minesweeper.
The player will be given a grid of a certain size, e.g., `5 * 7`, in which all squares are initially covered. E.g.,
```
#######
#######
#######
#######
#######
```
There will be mines under some of the squares. E.g.,
```
    X
   X
      X
XX  XXX
  X  X
```
and the player's goal is to uncover all of the clear squares without landing on a mine.
Each time they uncover a clear square, they will be shown the number of mines on the 4 neighbouring squares. E.g., if they uncover `row 2, column `5` as their first guess, they will see
```
#######
####2##
#######
#######
#######
```
due to the mine above and to the left of that square.

If the next square they uncover is `row 3, column 5` then they will see
```
#######
####2##
####1##
#######
#######
```
due to the one mine beneath that below... and so on, until either the player hits a mine or uncovers all the clear squares and wins the game.

1. Decide how to represent the game state, including

    - mine locations
    - which squares are uncovered
    - how many mines there are in total (so you can determine when the game is won)

    Hint: one way could be to use a 2d array (or two) to represent the state but, of course, there are other ways.

1. Populate the board -- you may want to do this randomly:

    ```c++
#include <time.h> // for the random seed
...
    // then in main, set the seed
    srand(time(NULL));

    // for each square in the grid, decide whether it wiss contain a mine
    bool hasMine = (rand() % 5) == 0; // one in five chance of there being a mine on the square
    ```

1. User input: the player will need to be able to input the position of the square they want to reveal.
1. Calculate the number of mines on the four neighbouring squares.
1. Game loop: the board should be printed, and the player should be prompted for input repeatedly.
1. Win / lose condition: the game should run until either the player wins (uncover all clear squares) or lose (hit a mine) -- when the game is over, the player should be informed whether they win or lose.

