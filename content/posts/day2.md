---
title: "Day 2 - #100daysofcode"
date: 2023-08-16T20:11:20+02:00
draft: false
---
Im reading the book C programming by K.N. King. At the end of each chapter he has written a good amount of (for now?) short exercises followed by programming projects.
Im currently on the chapter C fundamentals, which is going through the general form of a simple program, comments and finally variables and assignments.

Two of the projects regarded polynomial values which I had no previous knowledge of. After a few searches I managed to figure out what a polynomial expression was, and I managed to produce the following code together with an improved version, with better readability and maintainability.

```C
#include <stdio.h>

int main(void)
{
    int x, value;

    // Get input from the user
    printf("Enter a value: ");
    scanf("%d", &x);

    // Calculate the polynomial value
    value = 3 * (x * x * x * x * x) + 2 * (x * x * x * x) - 5 * (x * x * x) - (x * x) + 7 * x - 6

    // Print the result
    printf("Value of polynomial: %d\n", value);
}
```

```C
#include <stdio.h>

int main(void)
{
    int inputValue, polynomialValue;

    // Get input from the user
    printf("Enter a value: ");
    scanf("%d", &inputValue);

    // Calculate the polynomial value step by step
    int term1 = 3 * (inputValue * inputValue * inputValue * inputValue * inputValue);
    int term2 = 2 * (inputValue * inputValue * inputValue * inputValue);
    int term3 = 5 * (inputValue * inputValue * inputValue);
    int term4 = inputValue * inputValue;
    int term5 = 7 *inputValue;

    polynomialValue = term1 + term2 - term3 - term4 + term5 - 6;

    // Print the result
    printf("Value of polynomial: %d\n", polynomialValue);

    return 0;
}
```