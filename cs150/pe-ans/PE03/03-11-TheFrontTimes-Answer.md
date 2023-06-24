Given an input string and a non-negative int n, we'll say that the front of the string is the first 3 chars, or whatever is there if the string is less than length 3. Set result to n copies of the front;

* for input of "Chocolate", 2 → "ChoCho"
* for input of "Chocolate", 3 → "ChoChoCho"
* for input of "Abc", 3 → "AbcAbcAbc"

```cpp
#include <string>
using std::string;

/**
 *  Given an input string and a non-negative int n,
 *  we'll say that the front of the string is the first
 *  3 chars, or whatever is there if the string is less
 *  than length 3. Set result to n copies of the front
 */
string front_times(const string& str, int n)
{
	string result;
   // Your code goes here
	string front = str.substr(0, 3); // take the first 3 characters or whatever is there if the string is less than length 3
   for(size_t i {0}; i < n; ++i)
   {
       result += front; // append the front to the result n times
   }
   
    return result;
}
```

[frontTimes.cpp](https://codecheck.io/files/23020920341l81svyfw80vsnck780z35vof)

|Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|front_times|"Chocolate", 2|"ChoCho"|"ChoCho"|
|pass|front_times|"Chocolate", 3|"ChoChoCho"|"ChoChoCho"|
|pass|front_times|"Abc", 3|"AbcAbcAbc"|"AbcAbcAbc"|

This code first defines the "front" of the string as the first three characters, or fewer if the string has a length less than 3. Then it appends the "front" to the result string `n` times.