// You are given 2 ints, a and b; return their sum. However, "teen" values in the range 13..19 inclusive, are extra lucky. So if either value is a teen, just return 19.

 // * input of 3, 4 → 7
 // * input of 10, 13 → 19
 // * input of 13, 2 → 19

```cpp
/**
 *  You are given 2 ints, a and b; return their sum. 
 *  However, "teen" values in the range 13..19 inclusive, 
 *  are extra lucky. So if either value is a teen, just return 19. 
 */
int teen_sum(int a, int b)
{
    int result;
   
    // ---- YOUR CODE GOES ONLY BELOW THIS LINE
    // Add your code here
    if ((a >= 13 && a <= 19) || (b >= 13 && b <= 19)) { result = 19; }
    else { result = a + b; }
    return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|teen_sum|3, 4|7|7|
|pass|teen_sum|10, 13|19|19|
|pass|teen_sum|13, 2|19|19|

Score

3/3
\*/

// https://codecheck.io/files/23020821417ankrgke226asoknuxvbwudpp