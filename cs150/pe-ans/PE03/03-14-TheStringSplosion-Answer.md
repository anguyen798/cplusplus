Given a non-empty string like "Code" set result to a string like "CCoCodCode".

* for input of "Code" → "CCoCodCode"
* for input of "abc" → "aababc"
* for input of "ab" → "aab"

```cpp
#include <string>
using std::string;

/**
 *  Given a non-empty string like "Code" 
 *  set result to a string like "CCoCodCode".  
 */
string string_splosion(const string& str)
{
    string result;
  // Add your code here
    // Outer loop for each character in the string
    for(size_t i {0}, len {str.size()}; i < len; ++i)
    {
        // Inner loop to construct substring up to the current character
        for(size_t j {0}; j <= i; ++j)
        {
            result += str.at(j);
        }
    }
    return result;
}
```

[stringSplosion.cpp](https://codecheck.io/files/2302092318376z5dsjt4m0dvt66wudl1mmr)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|string_splosion|"Code"|"CCoCodCode"|"CCoCodCode"|
|pass|string_splosion|"abc"|"aababc"|"aababc"|
|pass|string_splosion|"ab"|"aab"|"aab"|

This problem can be solved by nested loops. The outer loop iterates through each character in the string, and the inner loop constructs a substring from the first character up to the current character in the outer loop. The inner loop appends these substrings to the result.

This code will return a string that consists of all prefixes of the input string concatenated together.
