---
title: "Day 10 - #100daysofcode"
date: 2023-08-24T21:03:36+02:00
draft: false
---

Working on if statements. 
Mental reminder to add more comments.

A program I wrote that converts 24h time to 12h.

```C
/* Convert 24h to 12h time */

#include <stdio.h>

int main(void)
{
    int hour, minute;

    printf("Enter a 24-hour time: ");
    scanf("%d:%d", &hour, &minute);

    if (hour >= 0 && hour <= 23) {

        if (hour <12) {
            printf("%02d:%02d AM\n", hour, minute);
        }
        else if (hour == 12) {
            printf("12:%02d PM\n", minute);
        }
        else {
            printf("%02d:%02d PM\n", hour -12, minute);
        }
    }
    else {
        printf("Invalid hour entered\n");
    }
}
```