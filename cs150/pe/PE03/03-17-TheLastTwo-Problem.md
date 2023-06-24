Given a string, set result to the count of the number of times that a substring length 2 appears in the string and also as the last 2 chars of the string, so "hixxxhi" yields 1 (we won't count the end substring).

* for input of "hixxhi" → 1
* for input of "xaxxaxaxx" → 1
* for input of "axxxaaxx" → 2

```cpp
#include <string>
using std::string;

/**
 *  Given a string, count the number of times that 
 *  the substring consisting of the last two characters
 *  appears elsewhere in the string. If the input is
 *  hixxxhi", then the result is 1, since "hi" appears
 *  one other time in the string. The substrings may
 *  overlap (as example 3 below), but do not count the
 *  ending substring.
 */
int last_two(const string& str)
{
   int result;
  // Add your code here

   return result;
}
```

[lastTwoProblem.cpp](https://codecheck.io/files/230209204262fj8d8l706cg2o59391dhbf2)