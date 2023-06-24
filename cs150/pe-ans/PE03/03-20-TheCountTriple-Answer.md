We'll say that a "triple" in a string is a char appearing three times in a row. Set result to the number of triples in the given string. The triples may overlap.

* for input of abcXXXabc" → 1
* for input of "xxxabyyyycd" → 3
* for input of "a" → 0

```cpp
#include <string>
using std::string;

/**
 *  Complete the function tripleThreat.
 *  We'll say that a "triple" in a string is a char 
 *  appearing three times in a row. Set result to the 
 *  number of triples in the given string. The triples 
 *  may overlap. 
 */
int count_triple(const string& str)
{
   int result = -1;

   // ---- YOUR CODE GOES ONLY BELOW THIS LINE
   result = 0; // result should start at 0 to return correctly
   for(size_t i {0}, len {str.size()}; i < len - 2; ++i)
   {
      if (len < 3)
      {
         return result;
         
      }
       else if(str.at(i) == str.at(i + 1) && str.at(i) == str.at(i + 2))
       {
           ++result;
       }
   }
   // ---- YOUR CODE GOES ONLY ABOVE THIS LINE
   
   return result;
}
```

[countTriple.cpp](https://codecheck.io/files/2302092104d079itf5mtbjas0h4vm6ujrjr)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|count_triple|"abcXXXabc"|1|1|
|pass|count_triple|"xxxabyyyycd"|3|3|
|pass|count_triple|"a"|0|0|

To solve this problem, you can iterate over the string and check if the current character and the next two characters are the same. If they are, you increment the counter for the number of triples. You have to be careful not to go out of bounds, so you only iterate up to the third last character.

In this code, we iterate over the string using an index `i`. For each character, we check if it's the same as the next two characters (`str[i+1]` and `str[i+2]`). If they are, we increment the `result` variable which counts the number of triples. We stop iterating at the third last character (`str.size() - 2`) to avoid going out of bounds.