Given an input string, count the number of words ending in 'y' or 'z' -so the 'y' in "heavy" and the 'z' in "fez" count, but not the 'y' in "yellow". Make sure that your comparison is not case sensitive. We'll say that a y or z is at the end of a word if there is not an alphabetic letter immediately following it.

* for input of "fez day" → 2
* for input of "day fez" → 2
* for input of "day fyyyz" → 2

```cpp
#include <string>
using std::string;

/**
 *  Given an input string, count the number of words ending 
 *  in 'y' or 'z' -so the 'y' in "heavy" and the 'z' in "fez" 
 *  count, but not the 'y' in "yellow". Make sure that your 
 *  comparison is not case sensitive. We'll say that a y 
 *  or z is at the end of a word if there is not an alphabetic 
 *  letter immediately following it. 
 *
 *  Do not use any string functions except for substr(), 
 *  at(), and size(), and isalpha() from <cctype>.
 *
 */
int count_yz(const string& str)
{
   int result;
  // Add your code here
    result = 0;  // to avoid error with size_t i initialization
    for(size_t i {0}, len = str.size(); i < len; ++i)
    {
        // We consider a word to have ended if the current character is not alphabetic
        // or if we've reached the end of the string
        if (!isalpha(str.at(i)) || i == len - 1)
        {
            char lastChar;
            if(i == 0 || i == len - 1)
            {
                lastChar = tolower(str.at(i));
            }
            else
            {
                lastChar = tolower(str.at(i - 1));
            }
            
            if (lastChar == 'y' || lastChar == 'z')
            {
                ++result;
            }
        }
    } 
   
   return result;
}
```

[countYZ.cpp](https://codecheck.io/files/23020921215sxy2vjyydptkb578yc0eav49)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|count_yz|"fez day"|2|2|
|pass|count_yz|"day fez"|2|2|
|pass|count_yz|"day fyyyz"|2|2|
|pass|count_yz|"day yak"|1|1|
|pass|count_yz|"!!day--yaz!!"|2|2|
|pass|count_yz|"yak zak"|0|0|

This problem involves iterating over the given string and checking if a word ends with 'y' or 'z'. Since we can't use any additional string functions, we need to manually keep track of the ends of words. A word is considered to have ended if we encounter a non-alphabetic character, or if we've reached the end of the string. In those cases, we check if the last character of the word was 'y' or 'z'. Here's the updated function:

This function counts the number of words in the input string that end with 'y' or 'z'. It handles cases in a case-insensitive manner and considers a word to have ended if there is a non-alphabetic character or it's the end of the string.