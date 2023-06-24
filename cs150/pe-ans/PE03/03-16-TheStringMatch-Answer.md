Given 2 strings, a and b, set result to the number of the positions where they contain the same length 2 substring. So "xxcaazz" and "xxbaaz" yields 3, since the "xx", "aa", and "az" substrings appear in the same place in both strings.

* for input of "xxcaazz", "xxbaaz" → 3
* for input of "abc", "abc" → 2
* for input of "abc", "axc" → 0

```cpp
#include <string>
using std::string;

/**
 *  Given 2 strings, a and b, set result to 
 *  the number of the positions where they contain 
 *  the same length 2 substring. So "xxcaazz" and "xxbaaz" 
 *  yields 3, since the "xx", "aa", and "az" substrings 
 *  appear in the same place in both strings.
 */
int string_match(const string& a, const string& b)
{
    int result;
  // Add your code here
	result = 0; // to avoid error with size_t i initialization
	// `?` is a ternary operator equivalent of int size;
	// if (a.size() < b.size()) a = {a.size();}
	// else {b.size();}
    size_t len = a.size() < b.size() ? a.size() : b.size();
    
    // Subtract 1 to not go beyond string length when checking pairs
    for(size_t i = 0; i < len - 1; ++i)
    {
        if (a.substr(i, 2) == b.substr(i, 2))
        {
            ++result;
        }
    }
   
    return result;
}
```

[stringMatch.cpp](https://codecheck.io/files/2302092352b1ousn9ux6rhe1bqf4d1o4xk4)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|string_match|"xxcaazz", "xxbaaz"|3|3|
|pass|string_match|"abc", "abc"|2|2|
|pass|string_match|"abc", "axc"|0|0|

In this problem, we need to iterate through both strings simultaneously, checking every pair of characters (length 2 substring) in each string. If the substrings are equal, we increment our result counter. We iterate until we've checked all pairs, which is until the size of the smaller string minus 1 (to account for zero-based indexing and pairs).

This function will return the number of positions where the strings a and b contain the same length 2 substring.