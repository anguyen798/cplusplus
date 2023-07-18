// Given two int values, return whichever value is larger. However, if the two values have the same remainder when divided by 5, then the return the smaller value. However, in all cases, if the two values are the same, return 0.

// * input of 2, 3 → 3
// * input of 6, 2 → 6
// * input of 3, 2 → 3

```cpp
/**
 *  Given two int values, return whichever value is larger. 
 *  However, if the two values have the same remainder when 
 *  divided by 5, then the return the smaller value. 
 *  However, in all cases, if the two values are the same, 
 *  return 0.
 */
int max_mod_five(int a, int b)
{
    int result;
    // Add your code here
    // Check for conditions according to the rules
    if (a == b) { result = 0; }
    else if (a % 5 == b % 5) { result = (a < b) ? a : b; }
    else { result = (a > b) ? a : b; }
    
    return result;
}
```
/*

Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|max_mod_five|2, 3|3|3|
|pass|max_mod_five|6, 2|6|6|
|pass|max_mod_five|3, 2|3|3|
|pass|max_mod_five|5, 5|0|0|

Score

4/4

\*/
// https://codecheck.io/files/2302082107b2k06r4ebtesp3wonpdv4qo4w