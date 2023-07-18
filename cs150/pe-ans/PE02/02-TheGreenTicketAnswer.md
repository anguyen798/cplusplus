// You have a green lottery ticket, with ints a, b, and c on it. If the numbers are all different from each other, the result is 0. If all of the numbers are the same, the result is 20. If two of the numbers are the same, the result is 10.

// * input of 1, 2, 3 → 0
// * input of 2, 2, 2 → 20
// * input of 1, 1, 2 → 10

```cpp
/**
 *  You have a green lottery ticket, 
 *  with ints a, b, and c on it. If the numbers are 
 *  all different from each other, the result is 0. 
 *  If all of the numbers are the same, the result 
 *  is 20. If two of the numbers are the same, 
 *  the result is 10. 
 */
int green_ticket(int a, int b, int c)
{
    int result;
     // Add your code here
     // Check for conditions according to the rules of the lottery ticket
     if (a == b && b == c) { result = 20; }
     else if (a == b || b == c || a == c) { result = 10; }
     else { result = 0; }
    
    return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|green_ticket|1, 2, 3|0|0|
|pass|green_ticket|2, 2, 2|20|20|
|pass|green_ticket|1, 1, 2|10|10|

Score

3/3
\*/

// https://codecheck.io/files/230208205551ebxs6bextyqlkiso5likc0f