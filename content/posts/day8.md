---
title: "Day 8 - #100daysofcode"
date: 2023-08-22T21:27:46+02:00
draft: false
---
Still on the chapter 'Selection Statements'. 
Worked some more on if statements today.

```C
#include <stdio.h>

int main(void)
{
    int number, digits, one, two, three, four;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (number <= 9)
        digits = 1;
    else if (number > 9 && number < 100)
        digits = 2;
    else if (number > 99 && number < 1000)
        digits = 3;
    else if (number > 999 && number < 10000)
        digits = 4;

    printf("The number %d has %d digits", number, digits);

    return 0;
}
```