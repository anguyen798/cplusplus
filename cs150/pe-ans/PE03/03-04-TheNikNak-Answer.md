Look for patterns like "nik" and "nak" in the input string-in other words a substring, length-3, starting with 'n' and ending with 'k'. Set result to a string where for all such words, the middle letter is gone, so "nikXnak" yields "nkXnk".

* for input of "nikXnak" → "nkXzp"
* for input of "noknok" → "nknk"
* for input of "nnnoknok" → "nnnknk"

```cpp
#include <string>
using std::string;

/**
 *  Look for patterns like "nik" and "nak" in 
 *  the input string-in other words a substring, 
 *  length-3, starting with 'n' and ending with 'k'. 
 *  Set result to a string where for all such words, 
 *  the middle letter is gone, so "nikXnak" yields "nkXnk"
 */
string nik_nak(const string& str)
{
    string result;
  // Add your code here
    size_t len {str.size()}, count {0}; // Index to track position in the result string
    result = string(len, ' '); // Assign result with same size filled with spaces
    for (size_t i {0}; i < len; ++i) 
    {
        // check if current character and next two characters form "n_k"
        if (i + 2 < len && str.at(i) == 'n' && str.at(i + 2) == 'k') 
        {
            result.at(count++) = 'n';
            result.at(count++) = 'k';
            i += 2; // skip the next two characters
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

[nikNak.cpp](https://codecheck.io/files/230209223150ppfzygyhcl1c21a5ldq50kf)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|nik_nak|"nikXnak"|"nkXnk"|"nkXnk"|
|pass|nik_nak|"noknok"|"nknk"|"nknk"|
|pass|nik_nak|"nnnoknok"|"nnnknk"|"nnnknk"|

This problem can be solved by iterating through the string and checking for each three-character sequence whether it starts with 'n' and ends with 'k'. If it does, then we add 'n', 'k' to the result and skip the middle character, otherwise we add the character to the result.

In this code, we are iterating over the string `str`. If the current character and the next two characters form a sequence that starts with 'n' and ends with 'k', we add 'n' and 'k' to the result and skip the next two characters. If the current three characters do not form such a sequence, we simply add the current character to the result. This process is repeated until we reach the end of the string.