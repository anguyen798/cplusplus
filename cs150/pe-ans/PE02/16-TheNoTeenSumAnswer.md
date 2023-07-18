// Given 3 int values, a b c, print their sum. However, if any of the values is a teen-in the range 13..19 inclusive- then that value counts as 0, except 15 and 16 do not count as a teens. You may write a separate helper function if you like. Define the helper above the problem function.

// * input of 1, 2, 3 → 6
// * input of 2, 13, 1 → 3
// * input of 2, 1, 14 → 3

```cpp
#include <string>
using std::string;

/**
 *  Given 3 int values, a b c, set result to their sum. 
 *  However, if any of the values is a teen-in the range 
 *  13..19 inclusive- then that value counts as 0, 
 *  except 15 and 16 do not count as a teens. 
 *  You may write a separate helper function if you like. 
 *  Define the helper above the problem function. 
 */
int fix_teen(int n)
{
   if ((n >= 13 && n <= 19) && (n != 15 && n != 16)) { return 0; }
   else { return n; }
}

int no_teen_sum(int a, int b, int c)
{
    int result;
     // Add your code here
     result = fix_teen(a) + fix_teen(b) + fix_teen(c);
    
    return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|no_teen_sum|1, 2, 3|6|6|
|pass|no_teen_sum|2, 13, 1|3|3|
|pass|no_teen_sum|2, 1, 14|3|3|

Score

3/3
\*/

// https://codecheck.io/files/2302091936av802ykhw9il9t5xnpibrfgrw