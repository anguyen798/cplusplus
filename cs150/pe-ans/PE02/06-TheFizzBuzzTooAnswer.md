// Given an int n, return the number followed by "!". So the int 6 returns "6!". Except if the number is divisible by 3 use "Fizz" instead of the number, and if the number is divisible by 5 use "Buzz", and if divisible by both 3 and 5, use "FizzBuzz". You can use to_string(n) to convert n into a string so you can concatenate.

// * input of 1 → "1!"
// * input of 2 → "2!"
// * input of 3 → "Fizz!"

```cpp
#include <string>
using namespace std;
/**
 *  Given an int n, return the number followed by "!". 
 *  So the int 6 returns "6!". Except if the number is 
 *  divisible by 3 use "Fizz" instead of the number, 
 *  and if the number is divisible by 5 use "Buzz", 
 *  and if divisible by both 3 and 5, use "FizzBuzz". 
 *  You can use to_string(n) to convert n into a string 
 *  so you can concatenate. 
 */
string fizz_buzz_too(int n)
{
    string result;
    // Add your code here
    if (n % 3 == 0 && n % 5 == 0) { result = "FizzBuzz!"; }
    else if (n % 3 == 0) { result = "Fizz!"; }
    else if (n % 5 == 0) { result = "Buzz!"; }
    else { result = to_string(n) + "!"; }
    
    return result;
}
```

/*

Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|fizz_buzz_too|1|"1!"|"1!"|
|pass|fizz_buzz_too|2|"2!"|"2!"|
|pass|fizz_buzz_too|3|"Fizz!"|"Fizz!"|
|pass|fizz_buzz_too|5|"Buzz!"|"Buzz!"|
|pass|fizz_buzz_too|15|"FizzBuzz!"|"FizzBuzz!"|

Score

5/5

\*/

// https://codecheck.io/files/2302082121707ir5s1njp1urm2tw7sygjdp