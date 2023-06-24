Given an input string, set result to a string where every appearance of the lowercase word "is" has been replaced with "is not". The word "is" should not be immediately preceded or followed by a letter -- so for example the "is" in "this" does not count.

* for input of "is test" → "is not test"
* for input of "is-is" → "is not-is not"
* for input of "This is right" → "This is not right"

```cpp
#include <string>
using std::string;

/**
 *  Given an input string, set result to a string where 
 *  every appearance of the lowercase word "is" has been 
 *  replaced with "is not". The word "is" should not be 
 *  immediately preceded or followed by a letter -- so 
 *  for example the "is" in "this" does not count.
 * 
 *  Do not use any string functions except for substr(), 
 *  at(), and size(). You may, however, use the <cctype>
 *  classification functions, such as isdigit() and isalpha().
 */
string is_not(const string& s)
{
   string result = "not done";

   // Add your code here
   result = "";  // set result to an empty string to return correctly
   for (size_t i {0}, len {s.size()}; i < len;)
   {
       if (i + 1 < len && s.at(i) == 'i' && s.at(i + 1) == 's' && 
          (i + 2 == len || !isalpha(s.at(i + 2))) &&
          (i == 0 || !isalpha(s.at(i - 1))))
       {
           result += "is not";
           i += 2;
       }
       else
       {
           result += s.at(i);
           i += 1;
       }
   }
   return result;
}
```

[notReplace.cpp](https://codecheck.io/files/23020920524wlozhfq7de54mnwrpu7hhyso)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|is_not|"is test"|"is not test"|"is not test"|
|pass|is_not|"is-is"|"is not-is not"|"is not-is not"|
|pass|is_not|"This is right"|"This is not right"|"This is not right"|

To solve this problem, you will need to traverse the string and check if "is" appears as a separate word. That means that it's either at the beginning/end of the string or it's surrounded by non-alphabetic characters. If it is, you replace it with "is not".

This code will append to the result either the word "is not" if "is" is found as a standalone word or the current character if not. Then it will increase the index depending on the number of characters processed.