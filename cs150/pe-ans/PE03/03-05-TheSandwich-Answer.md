A sandwich is two pieces of bread with something in between. Set result to the string that is between the first and last appearance of "bread" in the given string, or set it to the empty string "" if there are not two pieces of bread.

* for input of "breadjambread" → "jam"
*  for input of "xxbreadjambreadyy" → "jam"
* for input of "xxbreadyy" → ""

```cpp
#include <string>
using std::string;

/**
 *  A sandwich is two pieces of bread with something 
 *  in between. Set result to the string that is between 
 *  the first and last appearance of "bread" in the given 
 *  string, or set it to the empty string "" if there are 
 *  not two pieces of bread. 
 */
string bread_jam(const string& str)
{
    string result;
  // Add your code here
    string bread {"bread"};
    size_t strLen {str.size()}, breadLen {bread.size()};

    // find the first "bread"
    int i{0};
    while (i <= strLen - breadLen)
    {
        bool isMatch {true};
        for (size_t j {0}; j < breadLen; ++j)
        {
            if (str.at(i + j) != bread.at(j))
            {
                isMatch = false;
                break;
            }
        }
        if (isMatch) break;
        ++i;
    }

    // find the last "bread"
    size_t j {strLen - breadLen};
    while (j >= i)
    {
        bool isMatch = true;
        for (int k {0}; k < breadLen; ++k)
        {
            if (str.at(j + k) != bread.at(k))
            {
                isMatch = false;
                break;
            }
        }
        if (isMatch) break;
        --j;
    }

    if (j > i)
    {
        // if there are at least two "bread", get the sandwiched string
        for (int k {i + breadLen}; k < j; ++k)
        {
            result += str.at(k);
        }
    }
    return result; 
}
```

[sandWich.cpp](https://codecheck.io/files/23020922534fu10ghmqrpg7ecmrso27ly6g)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|bread_jam|"breadjambread"|"jam"|"jam"|
|pass|bread_jam|"xxbreadjambreadyy"|"jam"|"jam"|
|pass|bread_jam|"xxbreadyy"|""|""|

This problem can be solved by finding the first and last occurrence of the word "bread" in the string. If there are less than two occurrences of "bread", return an empty string. If there are two or more occurrences, return the substring between the first and last occurrence.

In this code, we first find the position of the first occurrence of "bread" in the string. If "bread" is not found, we return an empty string. Then we find the position of the last occurrence of "bread". If the first and last positions are the same, that means there is only one "bread", so we return an empty string. Otherwise, we return the substring between the first and last "bread".

The `find`, `rfind`, and `substr` member functions of the `string` class, which are not allowed by the problem constraints. Only the `substr()`, `at()`, `[]`, and `size()` member functions are allowed.

The following code uses a simple approach: it scans the string from both ends, looking for occurrences of "bread", then extracts the string between these occurrences.

In this solution, we first find the first and last occurrences of the word "bread" by scanning the string from the beginning and from the end. If there are at least two "bread", we then extract the substring between them by manually copying each character. If there is less than two "bread", we return an empty string.