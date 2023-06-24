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
	result = 0; // to avoid error with size_t i initialization
    size_t len {str.size()};
    string lastTwo = str.substr(len - 2);

    // Exclude last two characters from iteration
    for(size_t i {0}; i < len - 2; ++i)
    {
        if (str.substr(i, 2) == lastTwo)
        {
            ++result;
        }
    }

   return result;
}
```

[lastTwoProblem.cpp](https://codecheck.io/files/230209204262fj8d8l706cg2o59391dhbf2)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|last_two|"hixxhi"|1|1|
|pass|last_two|"xaxxaxaxx"|1|1|
|pass|last_two|"axxxaaxx"|2|2|

To solve this problem, we'll need to extract the last two characters from the string, then iterate through the string (excluding the last two characters) and compare every pair of characters with the extracted pair. We increment our counter if we find a match.

This function counts the number of times the substring consisting of the last two characters appears elsewhere in the string, not including the final occurrence of that substring.