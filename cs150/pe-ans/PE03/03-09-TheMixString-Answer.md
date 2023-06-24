Given two input strings, A and B, create a bigger string made of the first char of A, the first char of B, the second char of A, the second char of B, and so on. Any leftover chars go at the end of the result.

* for input of "abc", "xyz" → "axbycz"
* for input of "Hi", "There" → "HTihere"
* for input of "xxxx", "There" → "xTxhxexre"

```cpp
#include <string>
using std::string;

/**
 *  Given two input strings, A and B, create a bigger 
 *  string made of the first char of A, the first char of B, 
 *  the second char of A, the second char of B, and so on. 
 *  Any leftover chars go at the end of the result. 
 */
string mix_string(const string& a, const string& b)
{
   string result;
   // ---- YOUR CODE GOES ONLY BELOW THIS LINE
   size_t lenA {a.size()}, lenB {b.size()}, minLength, i {0};
   minLength = lenA < lenB ? lenA : lenB;

   for(i; i < minLength; ++i)
   {
       result += a.at(i);
       result += b[i];
   }

   if(lenA > minLength)
   {
       result += a.substr(i);
   }
   else if(lenB > minLength)
   {
       result += b.substr(i);
   }
  // ---- YOUR CODE GOES ONLY ABOVE THIS LINE
   
   return result;
}
```

[mixString.cpp](https://codecheck.io/files/23020920482acg6zblh1rt3re7d6appj705)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|mix_string|"abc", "xyz"|"axbycz"|"axbycz"|
|pass|mix_string|"Hi", "There"|"HTihere"|"HTihere"|
|pass|mix_string|"xxxx", "There"|"xTxhxexre"|"xTxhxexre"|

The approach here is to loop through both strings as long as they have characters. For each iteration, we add one character from each string to the result. If one string is longer than the other, we add the remaining part of the longer string to the result after the loop.