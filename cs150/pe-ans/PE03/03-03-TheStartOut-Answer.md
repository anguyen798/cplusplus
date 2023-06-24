
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
    // Copy only valid chars to result
    size_t len {str.size()};
    result = string(len, ' ');
    int count {0};
    for (size_t i {0}; i < len; ++i)
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
            result.at(count++) = str.at(i);
        }
    } 

    // Trim result to contain only valid chars
    result = result.substr(0, count);
    
    return result;
}
```

[startOut.cpp](https://codecheck.io/files/2302092225owznnm3sirjg9i9uhe865n00)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|star_out|"ab\*cd"|"ad"|"ad"|
|pass|star_out|"ab\*\*cd"|"ad"|"ad"|
|pass|star_out|"sm\*eilly"|"silly"|"silly"|

This problem can be solved by iterating over the given string and adding each character to the result string unless the character is a star or its adjacent characters are stars.

In this code, we are iterating over the string `str`. If the current character is a star, or the previous character or the next character is a star, we ignore the current character. If none of these conditions are met, we add the current character to the result string. We repeat this process until we reach the end of the string.

In C++, there are two ways to increment a variable: pre-increment (`++count`) and post-increment (`count++`). The difference between these two lies in when the increment operation is actually performed relative to any other operations on that line.

**Pre-increment (`++count`)**: The variable is incremented first, and then its value is used in the expression. For instance, in the line `result.at(++count) = str.at(i);`, `count` is incremented before its value is used as an index to the `result` string. So if `count` was initially `0`, it becomes `1` before it's used as an index.

**Post-increment (`count++`)**: The variable's current value is used in the expression first, and then the variable is incremented. So, in the line `result.at(count++) = str.at(i);`, the current value of `count` is used as an index to the `result` string, and then `count` is incremented. So if `count` was initially `0`, it's used as `0` first, and then it becomes `1`.

In the context of your code, using `count++` means that the first character of `str` that doesn't need to be removed will be placed at the 0th index of `result`, which is what you'd want. If you were to use `++count`, the first character would be placed at the 1st index, leaving the 0th index as it was initially (a whitespace character), which would be incorrect.