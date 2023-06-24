Suppose the string "yak" is unlucky. Given a string, set result to a version where all the "yak" are removed, but the "a" can be any char. The "yak" strings will not overlap.

* for input of "yakpak" → "pak"
* for input of "pakyak" → "pak"
* for input of "yak123ya" → "123ya"

```cpp
#include <string>
using std::string;

/**
 *  Suppose the string "yak" is unlucky. Given a string, 
 *  set result to a version where all the "yak" are removed, 
 *  but the "a" can be any char. The "yak" strings will not overlap.
 */
string string_yak(const string& str)
{
    string result;
  // Add your code here
    for(size_t i {0}, len {str.size()}; i < len; )
    {
        // if we encounter 'y' and there are at least 3 characters left 
        // and the third one is 'k', we skip the next three characters
        if(str.at(i) == 'y' && i + 2 < len && str[i+2] == 'k')
        {
            i += 3;
        }
        else
        {
            result += str.at(i);
            ++i;
        }
    }
   
    return result;
}
```

[stringYak.cpp](https://codecheck.io/files/23020923094b9xms74qqg159f0kg2u7lgl4)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|string_yak|"yakpak"|"pak"|"pak"|
|pass|string_yak|"pakyak"|"pak"|"pak"|
|pass|string_yak|"yak123ya"|"123ya"|"123ya"|

The problem can be solved by going through the string and checking for the pattern. When we encounter a 'y', we will check if the third character from there is 'k'. If it is, we will skip the next three characters; if not, we will append the 'y' to the result.

This code will remove all the "yak" patterns from the string, where 'a' can be any character. It will not remove any other characters.

