// Given 3 int values, a b c, print their sum. However, if one of the values is 13 then it does not count towards the sum and values to its right do not count. So for example, if b is 13, then both b and c do not count.

// * input of 1, 2, 3 → 6
// * input of 1, 2, 13 → 3
// * input of 1, 13, 3 → 1

```cpp
#include <string>
using std::string;

/**
 *  Given 3 int values, a b c, set result to their sum.
 *  However, if one of the values is 13 then it does
 *  not count towards the sum and values to its right do
 *  not count. So for example, if b is 13, then both b and
 *  c do not count.
 */
int lucky_sum(int a, int b, int c)
{
    int result;

     // Add your code here
     if (a == 13) { result = 0; }
     else if (b == 13) { result = a; }
     else if (c == 13) { result = a + b; }
     else { result = a + b + c; }
     
	return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|lucky_sum|1, 2, 3|6|6|
|pass|lucky_sum|1, 2, 13|3|3|
|pass|lucky_sum|1, 13, 3|1|1|

Score

3/3
\*/

// https://codecheck.io/files/2302091926ygkl35ktmrdkxke51nza84l7