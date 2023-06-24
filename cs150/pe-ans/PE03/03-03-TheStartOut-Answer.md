
Set result to a version of the given string, where for every star (\*) in the input string the star and the chars immediately to its left and right are gone. So "ab\*cd" yields "ad" and "ab**cd" also yields "ad".

* for input of "ab*cd" → "ad"
* for input of "ab**cd" → "ad"
* for input of "sm*eilly" → "silly"

```cpp
#include <string>
using std::string;

/**
 *  Set result to a version of the given string, 
 *  where for every star (*) in the input string the 
 *  star and the chars immediately to its left and right 
 *  are gone. So "ab*cd" yields "ad" and "ab**cd" also 
 *  yields "ad".
 *
 */
string star_out(const string& str)
{
    string result;
  // Add your code here
    for (size_t i {0}, len {str.size()}; i < len; ++i)
    {
        if (str.at(i) == '*') {
            continue;
        }
        else if (i > 0 && str.at(i - 1) == '*')
        {
            continue;
        }
        else if (i < len - 1 && str.at(i + 1) == '*')
        {
            continue;
        }
        else
        {
            result.push_back(str.at(i));
        }
    } 
    
    return result;
}
```

[startOut.cpp](https://codecheck.io/files/2302092225owznnm3sirjg9i9uhe865n00)

Calling with Arguments

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|star_out|"ab\*cd"|"ad"|"ad"|
|pass|star_out|"ab\*\*cd"|"ad"|"ad"|
|pass|star_out|"sm\*eilly"|"silly"|"silly"|

This problem can be solved by iterating over the given string and adding each character to the result string unless the character is a star or its adjacent characters are stars.

In this code, we are iterating over the string `str`. If the current character is a star, or the previous character or the next character is a star, we ignore the current character. If none of these conditions are met, we add the current character to the result string. We repeat this process until we reach the end of the string.