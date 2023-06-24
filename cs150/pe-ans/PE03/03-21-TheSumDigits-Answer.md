Given a string, set result to the sum of the digits 0-9 that appear in the string, ignoring all other characters. Return 0 if there are no digits in the string.

* for input of "aa1bc2d3" → 6
* for input of "aa11b33" → 8
* for input of "Chocolate" → 0

```cpp
#include <string>
#include <cctype>
using namespace std;

/**
 *  Given a string, set result to the sum of 
 *  the digits 0-9 that appear in the string, 
 *  ignoring all other characters. Return 0 if 
 *  there are no digits in the string. 
 */
int sum_digits(const string& str)
{
    int result;
  // Add your code here
     result = 0; // result should start at 0 to return correctly
     for (char c : str) 
    {
        if (isdigit(c)) 
        {
            result += c - '0';
        }
    }  
    return result;
}
```

[sumDigits.cpp](https://codecheck.io/files/230210240734cgify30km5u49fdntly1k5d)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|sum_digits|"aa1bc2d3"|6|6|
|pass|sum_digits|"aa11b33"|8|8|
|pass|sum_digits|"Chocolate"|0|0|

You can iterate over the string, and each time you encounter a digit character (which can be checked using the `isdigit()` function), you add its numerical value to the sum. The numerical value of a digit character can be obtained by subtracting the ASCII value of the character '0' from the ASCII value of the digit character.

The `isdigit()` function is used to check if a character is a digit. If the character is a digit, it is subtracted from '0' to get the integer value of the digit, and that is added to the `result`.