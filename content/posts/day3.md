---
title: "Day 3 - #100daysofcode"
date: 2023-08-17T20:41:49+02:00
draft: false
---

On the last project of the chapter 'C fundamentals'.
Im writing a program that calculates the remaining balance on a loan after the first, second and third monthly payments, it also has to account for interest rate.

Im planing on finishing this project tomorrow to get a fresh start on a new chapter this coming weekend. The chapter that awaits is 'Formatted input/output'.


A program I wrote today that shows how to pay using the smallest number of bills.
It looks a bit crude in my opining, looking forward to writing more pretty code.

```C
#include <stdio.h>

int main(void)
{
    int inputValue;

    // Get input from the user
    printf("Enter a dollar amount: ");
    scanf("%d", &inputValue);

    // Calculate amount of bills
    int bill20 = inputValue / 20;
    inputValue -= bill20 * 20;

    int bill10 = inputValue / 10;
    inputValue -= bill10 * 10;

    int bill5 = inputValue / 5;
    inputValue -= bill5 * 5;

    int bill1 = inputValue;

    // Print number of bills
    printf("$20: %d\n", bill20);
    printf("$10: %d\n", bill10);
    printf("$5: %d\n", bill5);
    printf("$1: %d\n", bill1);

    return 0;
}
```