// You are driving a little too fast, and a police officer stops you. Write code to compute the result, encoded as an int value: 0=no ticket, 25=small ticket, 275=big ticket. If speed is 60 or less, there is no ticket. If speed is between 61 and 80 inclusive, the result is a small ticket. If speed is 81 or more, the result is a large ticket. Unless it is your birthday-on that day, your speed can be 5 higher in all cases.

// * input of 60, birthday=false → 0
// * input of 65, birthday=false → 25
// * input of 65, birthday=true → 0

```cpp
#include <string>
using std::string;

/**
 *  You are driving a little too fast, and a police 
 *  officer stops you. Write code to compute the result, 
 *  encoded as an int value: 0=no ticket, 25=small ticket, 
 *  275=big ticket. If speed is 60 or less, there is 
 *  no ticket. If speed is between 61 and 80 inclusive, 
 *  the result is a small ticket. If speed is 81 or more, 
 *  the result is a large ticket. Unless it is your birthday--
 *  on that day, your speed can be 5 higher in all cases. 
 */
int caught_speeding(int speed, bool is_birthday)
{
   int result;
   // Add your code here
   int limit1 {is_birthday ? 65 : 60};
   int limit2 {is_birthday ? 85 : 80};
   
   if (speed <= limit1)  { result = 0; } 
   else if (speed <= limit2)  { result = 25; } 
   else  { result = 275; }

   return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|caught_speeding|60, false|0|0|
|pass|caught_speeding|65, false|25|25|
|pass|caught_speeding|65, true|0|0|

Score

3/3
\*/

// https://codecheck.io/files/23020919394pa0f1ghhkbctl0kcvvd1gmdi