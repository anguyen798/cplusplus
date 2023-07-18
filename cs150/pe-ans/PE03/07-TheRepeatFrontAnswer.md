Given as input a string and an int n, set result to a string made of the first n characters of the string, followed by the first n-1 characters of the string, and so on. You may assume that n is between 0 and the length of the string, inclusive (i.e. n >= 0 and n <= str.length()).

* for input of "Chocolate", 4 → "ChocChoChC"
* for input of "Chocolate", 3 → "ChoChC"
* for input of "Ice Cream", 2 → "IcI"

```cpp
#include <string>
using std::string;

/**
 *  Given a string and an int n, create a new string 
 *  made of the first n characters of the original 
 *  string, followed by the first n-1 characters of 
 *  the original string, and so on. You may assume 
 *  that n is between 0 and the length of the string, 
 *  inclusive (i.e. n >= 0 and n <= str.length())
 */
string repeat_front(const string& str, int n)
{
   string result = "not done";

  // Add your code here
    result = "";  // Set result to an empty string
    for(int i {n}; i >= 0; --i)
    {
        result += str.substr(0, i);
    }
   
   return result;
}
```

[repeatFront.cpp](https://codecheck.io/files/23020921131lpd8k21cp87daqzoaruxesvx)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|repeat_front|"Chocolate", 4|"ChocChoChC"|"ChocChoChC"|
|pass|repeat_front|"Chocolate", 3|"ChoChC"|"ChoChC"|
|pass|repeat_front|"Ice Cream", 2|"IcI"|"IcI"|

In this code, we start a loop from `n` and decrement it on each iteration until we reach 0. On each iteration, we take a substring of the original string from the beginning to the `i-th` character and append it to the `result`. This way, we first add the first `n` characters, then the first `n-1` characters, and so on, until we add the first character.