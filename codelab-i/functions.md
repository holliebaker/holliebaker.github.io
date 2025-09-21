---
layout: codelab
---

## Functions

### Callculator app

Build a calculator app. Begin with the following starter code:
```c++
#include <iostream>
#include <limits>

using namespace std;

// variables to store the two input numbers
int a, b;

// definitions for functions
void add(); // adds a and b, prints result
void sub();
void mul();
void div();

int main()
{
    while (true) {
        char op;
        cin >> a >> op >> b;
        if (cin.fail()) {
            cin.clear();
            cin.ignore(numeric_limits<streamsize>::max(), '\n');

            continue;
        }

        switch (op) {
            case '+':
                add();

                break;
            case '-':
                sub();

                break;
            case '*':
                mul();

                break;
            case '/':
                div();

                break;
            default:
                cout << "unknown operator, " << op << endl;

                break;
        }
    }

    return 0;
}
```

Note that this code won't compile yet, because the four functions `add()`, `sub()`, `mul()` and `div()` aren't defined (only declared.

1. First, declare the four functions. It's conventional to do this below main.
1. Complete each of the functions to add, subtract, multiply and divide the two numbers `a` and `b` (you can assume these have been read from `cin` already) and print out the answer.
1. In general, global variables are bad practice. Move the line `int a, b;` into the bofe of `main()`. This will eliminate the problem of global variables, but will also break your program since now the four functions no longer have access to `a` and `b`. In order to fix this, modify the definitions, declarations and calls to `add`, `sub`, `mul` and `div` to pass in the two integers as arguments.
1. It is good practice to write functions that do exactly one thing. At the moment, the function `add` not only performs addition, but also prints the result. Modify `add` to *return* the result of the addition instead of printing it. Back in `main` you can store the result returned by `add`, and print it out. Repeat for the other three functions.

### Arrays

1. Declare an arry (type and size of your choice), e.g., `int numbers[100];`
1. Write (declare and define) a function `void set(int arr[], int i, int v);` which sets the element at index `i` to the value `v`. Note, make sure the types of `arr` and `v` match the type of array you declared in your program.

  **Caveat!** this function will modify an element of the array passed in as an argument. This won't work with primitive types such as 'int' and 'float'. I.e., try writing a functions `void test(int a)` which modifies the value of 'a'. If you call this function with a variable, you'll see that the value of the variable remains unchanged. This is because the argument `a` is *local* to the function 'test'.
2. Write a function `int get(int arr[], int i)`, which returns the element of the array at index 'i'.
3. Write another function `void print(int arr[], int length)` to print out all the elements of `arr` in order.

    Test your program. It's recommended that you only move onto the next step once you're comfortable with how this part works.
4. Now let's modify the program to handle 2-dimensional arrays, the catch is, the underlying array will still be one-dimensional. I.e., instead of creating an array of arrays, you'll treat a long array as a 2-dimensional array. E.g., an array with `12` elements can be treated as a 2d array with `3` rows and `4` columns as follows
```
 0  1  2  3
 4  5  6  7
 8  9 10 11
```

Accessing elements involves a calculation based on the `width` of the grid, e.g.,
- If you wanted to get the element at row `0` column `1`, you'd retrieve element `1` form the 1d array,
- if you wanted the element at row `1`, column `2`, you'd need element `6 = 1 * 4 + 2 = 1 * width + 2 = rowIndex * width + columnIndex`,
- and if you wanted the element from row 2, column `0`, you'd retrieve element `8 = 2 * 4 + 0 = 2 * width + 0 = rowIndex * width + columnIndex`.

While these calculations aren't exactly complicated, it would be more convenient to simply ask for element `2` `0`. With this in mind, modify your functions to represent a 2d array. I.e., implement

- `int get(int arr[], int row, int col, int width)`
- `void set(int arr[], int row, int col, int value, int width)`
- 'void print(int arr[], int width, int height)`

### Hash table


