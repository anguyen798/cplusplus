// You have a red lottery ticket showing ints a, b, and c, each of which is 0, 1, or 2. If they are all the value 2, the result is 10. Otherwise if they are all the same, the result is 5. Otherwise so long as both b and c are different from a, the result is 1. Otherwise the result is 0.

// * input of 2, 2, 2 → 10
// * input of 2, 2, 1 → 0
// * input of 0, 0, 0 → 5

```cpp
/**
 *  You have a red lottery ticket showing ints a, b, 
 *  and c, each of which is 0, 1, or 2. If they 
 *  are all the value 2, the payout is 10. 
 *  Otherwise if they are all the same, the 
 *  payout is 5. Otherwise so long as both b and 
 *  c are different from a, the payout is 1. 
 *  Otherwise the payout is 0. 
 */
int red_ticket(int a, int b, int c)
{
    int payout;
   // Add your code here
   if (a == 2 && b == 2 && c == 2) { payout = 10; }
   else if (a == b && b == c) { payout = 5; }
   else if (a != b && a != c) { payout = 1; }
   else { payout = 0;}
    
   return payout;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|red_ticket|2, 2, 2|10|10|
|pass|red_ticket|2, 2, 1|0|0|
|pass|red_ticket|0, 0, 0|5|5|

Score

3/3

\*\

// https://codecheck.io/files/2302082101culya0gyed7djl1jv7j6q47xc