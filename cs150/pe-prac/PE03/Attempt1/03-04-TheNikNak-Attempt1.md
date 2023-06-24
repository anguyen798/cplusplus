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
   
    return result;
}
```

[nikNak.cpp](https://codecheck.io/files/230209223150ppfzygyhcl1c21a5ldq50kf)