---
title: "Day 5 - #100daysofcode"
date: 2023-08-19T21:06:58+02:00
draft: false
---

Feeling good after finishing the chapter 'Formatted input/output'.

Im trying my best to implement solutions ive learned in the current and previous chapters, and not skip ahead.

The following code I wrote looks like an absolute mess, but it works. Im looking forward to learning more elegant solutions.

```C
#include <stdio.h>

int main(void)
{
    int num1, num2, num3, num4, num5;
    int num6, num7, num8, num9, num10;
    int num11, num12, num13, num14, num15;
    int num16;

    // Get input from the user
    printf("Enter the numbers from 1 to 16 in any order: ");
    scanf("%d %d %d %d %d %d %d %d %d %d %d %d %d %d %d %d", &num1, &num2, &num3, &num4, &num5, &num6, &num7, &num8, &num9, &num10, &num11, &num12, &num13, &num14, &num15, &num16);

    // Prints the numbers in a 4 by 4 arrangement
    printf("%2d %2d %2d %2d\n%2d %2d %2d %2d\n%2d %2d %2d %2d\n%2d %2d %2d %2d\n", num1, num2, num3, num4, num5, num6, num7, num8, num9, num10, num11, num12, num13, num14, num15, num16);

    // Calculate sums
    int row1 = num1 + num2 + num3 + num4;
    int row2 = num5 + num6 + num7 + num8;
    int row3 = num9 + num10 + num11 + num12;
    int row4 = num13 + num14 + num15 + num16;

    int column1 = num1 + num5 + num9 + num13;
    int column2 = num2 + num6 + num10 + num14;
    int column3 = num3 + num7 + num11 + num15;
    int column4 = num4 + num8 + num12 + num16;

    int diagonal1 = num1 + num6 + num11 + num16;
    int diagonal2 = num4 + num7 + num10 + num13;

    // Print sums
    printf("Row sums: %d %d %d %d\n", row1, row2, row3, row4);
    printf("Column sums: %d %d %d %d\n", column1, column2, column3, column4);
    printf("Diagonal sums: %d %d\n", diagonal1, diagonal2);

    return 0;
}
```