// Given an input string str, if the string starts with "f" (either upper or lowercase), print "Fizz". If the string ends with "b" (either upper or lowercase), print "Buzz". If both the "f" and "b" conditions are true, print "FizzBuzz". In all other cases, print the string unchanged. Do not put the quotes around your output. I will do that in the problem.

// * input of "fig" → "Fizz"
// * input of "dib" → "Buzz"
// * input of "fib" → "FizzBuzz"


```cpp
#include <string>
using namespace std;
/**
 *  Given an input string str, if the string starts 
 *  with "f" (either upper or lowercase), return "Fizz". 
 *  If the string ends with "b" (either upper or lowercase), 
 *  return "Buzz". If both the "f" and "b" conditions are true, 
 *  return "FizzBuzz". In all other cases, return the string 
 *  unchanged.
 */
string fizz_string(const string& str)
{
    string result;
    // Add your code here
    size_t len {str.size()};
    bool startsWithF {(str.at(0) == 'f' || str.at(0) == 'F')};
    bool endsWithB {(str.at(len - 1) == 'b' || str.at(len - 1) == 'B')};
    
    if (startsWithF && endsWithB) { result = "FizzBuzz"; }
    else if (startsWithF) { result = "Fizz"; }
    else if (endsWithB) { result = "Buzz"; }
    else { result = str; }
    
    return result;
}
```

/*

Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|fizz_string|"fig"|"Fizz"|"Fizz"|
|pass|fizz_string|"dib"|"Buzz"|"Buzz"|
|pass|fizz_string|"fib"|"FizzBuzz"|"FizzBuzz"|
|pass|fizz_string|"steve"|"steve"|"steve"|

Score

4/4

\*/

// https://codecheck.io/files/2302082129afo8be9upb4nwzy0fjeo8815b