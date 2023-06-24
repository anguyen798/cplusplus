Given a string and a non-empty word string, set result to a version of the original string where all chars have been replaced by pluses ("+"), except for appearances of the word string which are preserved unchanged.

* for input of "12xy34", "xy" → "++xy++"
* for input of "12xy34", "1" → "1+++++"
* for input of "12xy34xyabcxy", "xy" → "++xy++xy+++xy"

```cpp
#include <string>
using std::string;

/**
 *  Given a string and a non-empty word string, set result 
 *  to a version of the original string where all chars 
 *  have been replaced by pluses ("+"), except for appearances 
 *  of the word string which are preserved unchanged. 
 */
string plus_out(const string& str, const string& word)
{
   string result = "not done";
   
  // Add your code here
    result = "";  // set result to empty string to return correctly
    size_t strLen {str.size()}, wordLen {word.size()};

    for (size_t i {0}; i < strLen;)
    {
        bool match = true;
        for (size_t j {0}; j < wordLen; ++j)
        {
            if (i + j >= strLen || str.at(i + j) != word.at(j))
            {
                match = false;
                break;
            }
        }

        if (match)
        {
            result += word;
            i += wordLen;
        }
        else
        {
            result += '+';
            ++i;
        }
    }
   
   return result;
}
```

[plusOut.cpp](https://codecheck.io/files/230209205965adg18jrctd8fjcm45euq96r)

|      | Name     | Arguments             | Actual          | Expected        |
| ---- | -------- | --------------------- | --------------- | --------------- |
| pass | plus_out | "12xy34", "xy"        | "++xy++"        | "++xy++"        |
| pass | plus_out | "12xy34", "1"         | "1+++++"        | "1+++++"        |
| pass | plus_out | "12xy34xyabcxy", "xy" | "++xy++xy+++xy" | "++xy++xy+++xy" |
|      |          |                       |                 |                 |

The logic to solve this problem is to iterate over the original string, and at each position, check whether the word is present. If the word is found, append the entire word to the result string and update the iterator position to after the word. If the word is not found at the current position, simply append a "+" character to the result.

In this code, the `while` loop iterates over the input string `str`. If the word is found, we append '+' characters for each character before the word, then append the word itself, and move the pointer to the end of the word. This process continues until we reach the end of the string. If the word is not found, we simply append '+' characters for the remaining characters in the string.

The `find` and `append` member functions of the `string` class, which are not allowed by the problem constraints. Only the `substr()`, `at()`, `[]`, and `size()` member functions are allowed.

In this solution, we iterate over the input string, checking at each position if it matches the provided word. If it does, we add the word to the result string and move our position by the length of the word. If it doesn't, we add a '+' to the result string and move to the next position.