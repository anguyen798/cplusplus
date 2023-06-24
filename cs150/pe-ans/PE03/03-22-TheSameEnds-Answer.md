Given a string, set result to the longest substring that appears at both the beginning and end of the string without overlapping. For example, given the input "abXab", then result "ab".

* for input of "abXYab" → "ab"
* for input of "xx" → "x"
* for input of xxx" → "x"

```cpp
#include <string>
using namespace std;

/**
 *  Given a string, return the longest 
 *  substring that appears at both the beginning 
 *  and end of the string without overlapping. For 
 *  example, given the input "abXab", return "ab".
 *  Do not use any string functions except for substr(), 
 *  at(), [], and size().
 */
string same_ends(const string& str)
{
    string result = "NOT DONE";
    // Add your code here
    result = ""; // set result to an empty string
    for (size_t len {str.size()}, i {len / 2}; i > 0; --i)
    {
        if (str.substr(0, i) == str.substr(len - i, i))
        {
            result = str.substr(0, i);
            break;
        }
    }
    return result;
}
```

[sameEnds.cpp](https://codecheck.io/files/23021024111wo43c96la7h5smnpo4atw0sj)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|same_ends|"abXYab"|"ab"|"ab"|
|pass|same_ends|"xx"|"x"|"x"|
|pass|same_ends|"xxx"|"x"|"x"|

In order to find the longest substring that appears at both the beginning and end of the string, you can create a loop that checks for substrings of decreasing size until it finds one that matches.

The outer loop should start at the length of the string divided by 2 (because the substring cannot be longer than this), and should decrement down to 0.

The inner loop checks if the substring of the current length from the start of the string matches the substring of the same length from the end of the string. If it does, it sets the result to this substring and breaks the loop.

This code starts checking from the middle of the string and decreases the size of the substring it checks each iteration. It stops when it finds a match or when it checks all possible sizes.