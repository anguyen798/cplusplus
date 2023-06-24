Given a string, set result to a new string made of every other char starting with the first, so "Hello" yields "Hlo".

* for input of "Hello" → "Hlo"
* for input of "Hi" → "H"
* for input of "Heeololeo" → "Hello"

```cpp
#include <string>
using std::string;

/**
 *  Given a string, set result to a new string 
 *  made of every other char starting with the 
 *  first, so "Hello" yields "Hlo". 
 */
string string_bits(const string& str)
{
    string result;
  // Add your code here
    for(size_t i {0}, len {str.size()}; i < len; i += 2)
    {
        result += str.at(i);
    }
    
    return result;
}
```

[stringBits.cpp](https://codecheck.io/files/23020923123byrkw833uk413jzv2rtpwlp9)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|string_bits|"Hello"|"Hlo"|"Hlo"|
|pass|string_bits|"Hi"|"H"|"H"|
|pass|string_bits|"Heeololeo"|"Hello"|"Hello"|

The problem can be solved by iterating over the string and taking every other character starting from the first one. This can be done by incrementing the loop counter by 2 for each iteration.

This code will return a string made of every other character of the input string, starting with the first character.

