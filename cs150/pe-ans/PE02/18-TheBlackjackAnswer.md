// Given 2 int values greater than 0, print whichever value is nearest to 21 without going over. Print 0 if they both go over.

// * input of 19, 21 → 21
// * input of 21, 19 → 21
// * input of 19, 22 → 19

```cpp
/**
 *  You have been dealt two cards, a and b. 
 *  Each card has a value 0-100. Set the variable 
 *  nearest to whichever value is nearest to 21 
 *  without going over. Return 0 if both cards go over.
 */
int nearest(int a, int b)
{
    int nearest = 0;

    // Add your code here
    if (a > 21 && b > 21)  { nearest = 0; } 
    else if (a > 21)  { nearest = b; } 
    else if (b > 21)  { nearest = a; } 
    else  { nearest = (a > b) ? a : b; }
   
   return nearest;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|nearest|19, 21|21|21|
|pass|nearest|21, 19|21|21|
|pass|nearest|19, 22|19|19|

Score

3/3
\*/

// https://codecheck.io/files/23020919553h3rrl5jyo7g49v93co7ohx7n