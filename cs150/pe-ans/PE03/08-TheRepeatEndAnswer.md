Given as input string and an int N, set result a string made of N repetitions of the last N characters of the string. You may assume that N is between 0 and the length of the string, inclusive.

* for input of "Hello", 3 → "llollollo"
* for input of "Hello", 2 → "lolo"
* for input of "Hello", 1 → "o"

```cpp
#include <string>
using std::string;

/**
 *  Given as input string and an int N, set result 
 *  a string made of N repetitions of the last N characters 
 *  of the string. You may assume that N is between 0 and 
 *  the length of the string, inclusive. 
 */
string repeat_end(const string& str, int n)
{
   string result = "not done";
   
  // Add your code here
    result = "";  // set result to an empty string to return correctly
    string lastN {str.substr(str.length() - n)}; // get the last n characters
    for(int i {0}; i < n; ++i)
    {
        result += lastN;
    }
   
   return result;
}
```

[repeatEnd.cpp](https://codecheck.io/files/23020920564ub5dprbojbgty0c5av4kce3a)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|repeat_end|"Hello", 3|"llollollo"|"llollollo"|
|pass|repeat_end|"Hello", 2|"lolo"|"lolo"|
|pass|repeat_end|"Hello", 1|"o"|"o"|

In this code, we first create a substring of the last `n` characters from the original string. Then we create a loop that runs `n` times. In each iteration, we append the substring to the `result`. This gives us a string made of `n` repetitions of the last `n` characters of the string.