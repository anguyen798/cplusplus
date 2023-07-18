// Given three integers (a, b, and c), print the number of unique values among the three. For example:

// * for input of 18, 3, 4 → 3
// * for input of 6, 7, 6 → 2

```cpp
/**
 *  Given three integers (a, b, and c), 
 *  return the number of unique values among the three. 
 */
int unique(int a, int b, int c)
{
    int result;

    // Add your code here
        result = 1;
        if (b != a) { ++result; }
        if (c != a && c != b) { ++result; }
   
   return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|unique|18, 3, 4|3|3|
|pass|unique|6, 7, 6|2|2|
|pass|unique|7, 7, 7|1|1|

Score

3/3
\*/

// https://codecheck.io/files/2302092021bfl2tz5lhty962g57jf0ucpc8