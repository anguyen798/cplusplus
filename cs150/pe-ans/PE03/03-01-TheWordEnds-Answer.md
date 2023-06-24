Given a string and a non-empty word string, set result to a string made of each char just before and just after every appearance of the word in the string. Ignore cases where there is no char before or after the word, and a char may be included twice if it is between two words. Do not do any printing.

* for input of "abcXY123XYijk", "XY" → "c13i"
* for input of "XY123XY", "XY" → "13"
* for input of "XY1XY", "XY" → "11"

```cpp
#include <string>
using std::string;

/**
 *  Given a string and a non-empty word string, 
 *  set result to a string made of each char 
 *  just before and just after every appearance 
 *  of the word in the string. Ignore cases where 
 *  there is no char before or after the word, and 
 *  a char may be included twice if it is between two 
 *  words.
 *
 */
string word_ends(const string& str, const string& word)
{
    string result;
  // Add your code here
    size_t strLen {str.size()}, wordLen {word.size()};

    for (int i {0}; i <= strLen - wordLen;)
    {
        bool match = true;
        for (int j {0}; j < wordLen; ++j)
        {
            if (str.at(i + j) != word.at(j))
            {
                match = false;
                break;
            }
        }

        if (match)
        {
            if (i != 0)
            {
                result += str[i - 1];
            }
            if (i + wordLen < strLen)
            {
                result += str[i + wordLen];
            }
            i += wordLen;
        }
        else
        {
            ++i;
        }
    }
   
    return result;
}
```

[wordsEndProblem.cpp](https://codecheck.io/files/23020921362lyahmk5rxjjf6t9zgtlz91qq)

|      | Name      | Arguments             | Actual | Expected |
| ---- | --------- | --------------------- | ------ | -------- |
| pass | word_ends | "abcXY123XYijk", "XY" | "c13i" | "c13i"   |
| pass | word_ends | "XY123XY", "XY"       | "13"   | "13"     |
| pass | word_ends | "XY1XY", "XY"         | "11"   | "11"     |
|      |           |                       |        |          |

The function will iterate through the given string and when it finds a match with the word, it will append the characters just before and just after the word to the result string.

In this code, we are iterating through the string `str` and at each position, we check if the word is found. If the word is found, we add the character before the word and after the word to the `result` string and move the index pointer to the end of the word. This process repeats until we reach the end of the string or there is no word left to be found.

As per the constraints, you're not allowed to use the `find()` function, and also you are asked to not use any member function other than `substr()`, `at()`, `[]`, and `size()`.

This solution iterates over the input string and tries to match the word at each position. If it finds a match, it adds the character before and after the word to the result string, if they exist. It then skips over the word. If it doesn't find a match, it moves to the next position.
