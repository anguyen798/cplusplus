Given as input two strings, word and a separator, set result to a big string made of count occurrences of the word, separated by the separator string.

* for input of "Word", "X", 3 → "WordXWordXWord"
* for input of "This", "And", 2 → "ThisAndThis"
* for input of "This", "And", 1 → "This"

```cpp
#include <string>
using std::string;

/**
 *  Given as input two strings, word and a separator, 
 *  set result to a big string made of count occurrences 
 *  of the word, separated by the separator string. 
 */
string repeat_separator(const string& word, const string& separator, int count)
{
    string result;
  // Add your code here
    for(int i {0}; i < count; ++i)
    {
        result += word;
        if (i < count - 1)
        { // do not add separator after the last word
            result += separator;
        }
    }
   
    return result;
}
```

[repeatSeparator.cpp](https://codecheck.io/files/230209225988ltfgyodjxlsyb5mjhf5l0rl)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|repeat_separator|"Word", "X", 3|"WordXWordXWord"|"WordXWordXWord"|
|pass|repeat_separator|"This", "And", 2|"ThisAndThis"|"ThisAndThis"|
|pass|repeat_separator|"This", "And", 1|"This"|"This"|

This problem can be solved by repeating the word `count` times and inserting the separator between each repetition of the word.

In this code, we're creating a loop that iterates `count` times. On each iteration, we append the word to the `result`. If the current iteration is not the last, we also append the separator to the `result`.