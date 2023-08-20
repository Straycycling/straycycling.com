---
title: "Day 6 - #100daysofcode"
date: 2023-08-20T20:43:28+02:00
draft: false
---

I have been learning expressions and selection statements today.
The selection statements im learning right are the most fun so far in this book and im looking forward to integrating loops, which are coming soon!


I wrote this program that converts a base 10 number to base 8
```C
/* Converting from base 10 to base 8 */
#include <stdio.h>

int main(void)
{
    int number;
    int octalDigit1, octalDigit2, octalDigit3, octalDigit4, octalDigit5;

    printf("Enter a number between 0 and 32767: ");
    scanf("%d", &number);

    // Calculate octal digits
    octalDigit5 = number % 8;
    number = number / 8;

    octalDigit4 = number % 8;
    number = number / 8;

    octalDigit3 = number % 8;
    number = number / 8;

    octalDigit2 = number % 8;
    number = number / 8;

    octalDigit1 = number % 8;

    // Output the octal number
    printf("In octal, your number is: %d%d%d%d%d\n", octalDigit1, octalDigit2, octalDigit3, octalDigit4, octalDigit5);

    return 0;
}
```