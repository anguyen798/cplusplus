// You have a blue lottery ticket, with ints a, b, and c on it. This makes three pairs, which we'll call ab, bc, and ac. Consider the sum of the numbers in each pair. If any pair sums to exactly 10, the result is 10. Otherwise if the ab sum is exactly 10 more than either bc or ac sums, the result is 5. Otherwise the result is 0. You will print the result. Here are some samples.

// * input of 9, 1, 0 → 10
// * input of 9, 2, 0 → 0
// * input of 6, 1, 4) → 10

```cpp
/**
 *  You have a blue lottery ticket, 
 *  with ints a, b, and c on it. This makes 
 *  three pairs, which we'll call ab, bc, and ac. 
 *  Consider the sum of the numbers in each pair. 
 *  If any pair sums to exactly 10, the result 
 *  is 10. Otherwise if the ab sum is exactly 
 *  10 more than either bc or ac sums, the 
 *  result is 5. Otherwise the result is 0. 
 */
int blueTicket(int a, int b, int c)
{
    int payout;
     // Add your code here
     // Calculate sums of the pairs
     int ab {a + b};
     int bc {b + c};
     int ac {a + c};
     
     // Check for conditions according to the rules of the lottery ticket
     if (ab == 10 || bc == 10 || ac == 10) { payout = 10; }
     else if (ab - bc == 10 || ab - ac == 10) { payout = 5;}
     else { payout = 0; }
   
    return payout;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|blueTicket|9, 1, 0|10|10|
|pass|blueTicket|9, 2, 0|0|0|
|pass|blueTicket|6, 1, 4|10|10|

Score

3/3
\*/


// https://codecheck.io/files/230208171291t3o6nzn9m49s5zu03s6bc9g