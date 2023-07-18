// Given 2 ints, a and b, print their sum. However, sums in the range 10..19 inclusive, are forbidden, so in that case just print 20.

// * input of 3, 4 → 7
// * input of 9, 4 → 20
// * input of 10, 11 → 21

```cpp
/**
 *  Given 2 ints, a and b, print their sum. 
 *  However, sums in the range 10..19 inclusive, 
 *  are forbidden, so in that case just print 20. 
 */
int sorta_sum(int a, int b)
{
    int result = 0;

    // Add your code here
    int sum {a + b};
    if (sum >= 10 && sum <= 19) { result = 20; }
    else { result = sum; }
   
   return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|sorta_sum|3, 4|7|7|
|pass|sorta_sum|9, 4|20|20|
|pass|sorta_sum|10, 11|21|21|

Score

3/3
\*/

// https://codecheck.io/files/2302092009cnsajf5yrx4zhglyuymnltg9v