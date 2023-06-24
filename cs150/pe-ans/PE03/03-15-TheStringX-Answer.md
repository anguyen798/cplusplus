Given a string, set result to a version where all the "x" have been removed. Except an "x" at the very start or end should not be removed.

* for input of "xxHxix" → "xHix"
* for input of "abxxxcd" → "abcd"
* for input of "xabxxxcdx" → "xabcdx"

```cpp
#include <string>
using std::string;

/**
 *  Given a string, set result to a version 
 *  where all the "x" have been removed. Except an 
 *  "x" at the very start or end should not be removed.  
 */
string string_x(const string& str)
{
    string result;
  // Add your code here
    size_t len {str.size()};
    // Add the first character without checking
    if (!str.empty())
    {
        result += str.at(0);
    }

    // Iterate from the second to the second-to-last character
    for(size_t i {1}; i < len - 1; ++i)
    {
        // If the character is not 'x', append it to the result
        if (str.at(i) != 'x')
        {
            result += str.at(i);
        }
    }

    // Add the last character without checking
    if (len > 1)
    {
        result += str.at(len - 1);
    } 
    
    return result;
}
```

[stringX.cpp](https://codecheck.io/files/2302092325662ltflq8xu3wlctcxphiy4lw)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|string_x|"xxHxix"|"xHix"|"xHix"|
|pass|string_x|"abxxxcd"|"abcd"|"abcd"|
|pass|string_x|"xabxxxcdx"|"xabcdx"|"xabcdx"|

In this problem, we will iterate through the string from the second character up to the second-to-last character, skipping the first and the last character. If the character is not an 'x', we append it to the result. Then, we just need to add the first and the last character to the result without checking if they are 'x' or not.

This function will effectively remove all 'x' characters from the string, except those at the very start or end.
