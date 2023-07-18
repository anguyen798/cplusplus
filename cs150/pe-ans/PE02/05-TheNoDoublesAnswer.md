// Return the sum of two 6-sided dice rolls, each in the range 1..6. However, if has_doubles (the third value input) is true, and, if the two dice show the same value, increment one die to the next value, wrapping around to 1 if its value was 6. Here are some examples.

// * input of 2, 3, true → 5
// * input of 3, 3, true → 7
// * input of 3, 3, false → 6

```cpp
/**
 *  Return the sum of two 6-sided dice rolls, 
 *  each in the range 1..6. However, if no_doubles (the third parameter) 
 *  is true, and, if the two dice show the same value, increment one die 
 *  to the next value, wrapping around to 1 if its value was 6. 
 */
int no_doubles(int a, int b, bool has_doubles)
{
    int result;
    // Add your code here
    // Check for conditions according to the rules
    if (has_doubles && a == b) { a = a % 6 + 1; }
    result = a + b;
    
    return result;
}
```

/*

Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|no_doubles|2, 3, true|5|5|
|pass|no_doubles|3, 3, true|7|7|
|pass|no_doubles|3, 3, false|6|6|

Score

3/3

\*/


// https://codecheck.io/files/23020821144fyhnopj1ejq7ksucd0d71lrn