Given two input strings, base and remove, set result to a version of the base string where all instances of the remove string have been removed. You may assume that the remove string is length 1 or more. Remove only non-overlapping instances, so with "xxx" removing "xx" leaves "x".

* for input of "Hello there", "llo" → "He there"
* for input of "Hello there", "e" → "Hllo thr"
* for input of "Hello there", "x" → "Hello there"

```cpp
#include <string>
#include <cctype>
using namespace std;

/**
 *  Given two input strings, base and remove, 
 *  set result to a version of the base string 
 *  where all instances of the remove string have 
 *  been removed. This is not case sensitive. You 
 *  may assume that the remove string is length 
 *  1 or more. Remove only non-overlapping instances, 
 *  so with "xxx" removing "xx" leaves "x". 
 */
string without_string(const string& base, const string& remove)
{
    string result;
  // Add your code here
    size_t baseLen {base.size()}, removeLen {remove.size()};

    for (size_t i {0}; i < baseLen;)
    {
        bool match = true;
        if (baseLen - i >= removeLen)
        {
            for (int j {0}; j < removeLen; ++j)
            {
                if (tolower(base.at(i + j)) != tolower(remove.at(j)))
                {
                    match = false;
                    break;
                }
            }

            if (match)
            {
                i += removeLen;
            }
            else
            {
                result += base.at(i);
                ++i;
            }
        }
        else
        {
            result += base.at(i);
            ++i;
        }
    }
    
    return result;
}
```

[withoutString.cpp](https://codecheck.io/files/230210240278eo7mvnj4e5ddtps56xaqifp)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|without_string|"Hello there", "llo"|"He there"|"He there"|
|pass|without_string|"Hello there", "e"|"Hllo thr"|"Hllo thr"|
|pass|without_string|"Hello there", "x"|"Hello there"|"Hello there"|

This problem can be solved by iteratively checking and removing all occurrences of the "remove" string in the "base" string. We can use the built-in std::string::find and std::string::erase methods to achieve this. However, to make it case-insensitive, we need to create lower-case copies of both strings for searching. Below is the function that accomplishes this:

This function uses std::transform to convert the input strings to lowercase, allowing case-insensitive comparison. It then repeatedly uses std::string::find to find the position of the remove string in the base string, and std::string::erase to remove it. The process repeats until there are no more occurrences of the remove string left in the base string. Note that it also removes the matching substrings from the lower-case copy of the base string to keep it synchronized with the original string.