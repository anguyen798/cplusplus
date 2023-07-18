// Given 3 int values, a b c, print their sum. However, if one of the values is the same as another of the values, it does not count towards the sum.

// * input of 1, 2, 3 → 6
// * input of 3, 2, 3 → 2
// * input of 3, 3, 3 → 0

```cpp
#include <string>
using std::string;
/**
 *  Given 3 int values, a b c, set result to their sum. 
 *  However, if one of the values is the same as another 
 *  of the values, it does not count towards the sum. 
 */
int lone_sum(int a, int b, int c)
{
    int result;
     // Add your code here
     if (a == b && b == c) { result = 0; }
     else if (a == b) { result = c; }
     else if (a == c) { result = b; }
     else if (b == c) { result = a; }
     else { result = a + b + c; }
    
    return result;
}
```

/*
Calling with Arguments

||Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|lone_sum|1, 2, 3|6|6|
|pass|lone_sum|3, 2, 3|2|2|
|pass|lone_sum|3, 3, 3|0|0|

Score

3/3
\*/

// https://codecheck.io/files/230209193356i4j3yiuoiiz8dxxtibp1ama