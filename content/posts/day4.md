---
title: "Day 4 - #100daysofcode"
date: 2023-08-18T21:08:46+02:00
draft: false
---

Finished up 'C fundamentals' and started ' Formatted input/output' today.

First project was some basic formatting.
```C
#include <stdio.h>

int main(void)
{
    int mm, dd, yyyy;

    // Get input from the user in the form mm/dd/yyyy
    printf("Enter a date (mm/dd/yyyy) : ");
    scanf("%d/%d/%d", &mm, &dd, &yyyy);

    // Display the date in the form yyyymmdd
    printf("You entered the date %4.d%.2d%d", yyyy, mm, dd);

    return 0;
}
```

Upcoming formatting with multiple lines looks a bit confusing at the moment.