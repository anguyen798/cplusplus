// Given an integer as input, representing a month (1 for January, 2 for February, and so on), print the number of days in that month in a non-leap-year (that February always has 28 days).

// Month : Days
// 1 Jan : 31
// 2 Feb : 28
// 3 Mar : 31
// 4 Apr : 30
// 5 May : 31
// 6 Jun : 30
// 7 Jul : 31
// 8 Aug : 31
// 9 Sep : 30
// 10 Oct : 31
// 11 Nov : 30
// 12 Dec : 31

```cpp
/**
 *  Given an integer as input, representing a month 
 *  (1 for January, 2 for February, and so on), return
 *  the number of days in that month in a non-leap-year 
 *  (that February always has 28 days). 
 */
int days_in_month(int month)
{
    int result;

    // Add your code here
    switch (month)
    {
       case 1: 
       case 3:
       case 5:
       case 7:
       case 8:
       case 10:
       case 12: result = 31;
       break;
       
       case 4:
       case 6:
       case 9:
       case 11: result = 30;
       break;
       
       case 2: result = 28;
       break;
       
       default: result = 0;  // if invalid month is provided
    }
   
   return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|days_in_month|1|31|31|
|pass|days_in_month|2|28|28|
|pass|days_in_month|4|30|30|

Score

3/3
\*/

// https://codecheck.io/files/2302092027aa3bgsrpvsf5m4hdbwkfbs2kd