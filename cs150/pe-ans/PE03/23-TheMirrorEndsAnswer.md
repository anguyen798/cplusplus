Given a string, look for a mirror image (backwards) string at both the beginning and end of the given string. In other words, zero or more characters at the very beginning of the given string, and at the very end of the string in reverse order (possibly overlapping). For example, the string "abXYZba" has the mirror end "ab".

* for input of "abXYZba" → "ab"
* for input of "abca" → "a"
* for input of "aba" → "aba"

```cpp
#include <string>
using std::string;

/**
 *  Given a string, look for a mirror image (backwards) 
 *  string at both the beginning and end of the given 
 *  string. In other words, zero or more characters at the 
 *  very beginning of the given string, and at the very end 
 *  of the string in reverse order (possibly overlapping). 
 *  For example, the string "abXYZba" has the mirror end "ab".
 */
string mirror_ends(const string& str)
{
   string result;
   // Add your code here
   size_t i {0}, len {str.size()};

   while (i < len && str.at(i) == str.at(len - i - 1))
   {
       ++i;
   }

   result = str.substr(0, i);
   
   return result;
}
```

[mirrorEnds.cpp](https://codecheck.io/files/23020920459n9yy0lwabl9iuqdp6q27xt1l)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|mirror_ends|"abXYZba"|"ab"|"ab"|
|pass|mirror_ends|"abca"|"a"|"a"|
|pass|mirror_ends|"aba"|"aba"|"aba"|

To implement this, we need to compare characters at corresponding positions from the start and end of the string. When the characters stop matching, we have found our "mirror" string.

This solution scans the string from both ends toward the middle, comparing characters at corresponding positions. When it encounters a pair of characters that are not equal, it stops and returns the part of the string up to that point as the result.
