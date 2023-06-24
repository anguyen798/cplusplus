Set result to the number of times that the string "code" appears anywhere in the input given string, except we'll accept any letter for the 'd', so "cope" and "cooe" count.

* for input of "aaacodebbb" → 1
* for input of "codexxcode" → 2
* for input of "cozexxcope" → 2

```cpp
#include <string>
using std::string;

/**
 *  Set result to the number of times that the 
 *  string "code" appears anywhere in the input 
 *  given string, except we'll accept any letter 
 *  for the 'd', so "cope" and "cooe" count.
 */
int count_code(const string& str)
{
    int result;
  // Add your code here
   result = 0; // to avoid error with size_t i initialization
   for (size_t i {0}, len {str.size()}; i < len - 3; ++i)
   {
       if (str.at(i) == 'c' && str.at(i+1) == 'o' && str.at(i+3) == 'e')
       {
           ++result;
       }
   }  
   
    return result;
}
```

[countCode.cpp](https://codecheck.io/files/230209230485dil05w42eu2a0r0vzmhiour)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|count_code|"aaacodebbb"|1|1|
|pass|count_code|"codexxcode"|2|2|
|pass|count_code|"cozexxcope"|2|2|

This code scans through the input string `str` and for each position checks if there is a 'c' at that position, 'o' at the next position, and 'e' at the position two steps forward. If it is true, it counts as one occurrence. The check does not include the last three characters of the string as it can't form the desired pattern from there.