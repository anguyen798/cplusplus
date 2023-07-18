// You and your date are trying to get a table at a restaurant. The first input ("you") is the stylishness of your clothes, in the range 0..10, and the second ("date") is the stylishness of your date's clothes. The result getting the table is encoded as "no", "maybe", or "yes". If either of you is very stylish, 8 or more, then the result is yes. With the exception that if either of you has style of 2 or less, then the result is no. Otherwise the result is maybe.

// * input of 5, 10 → "yes"
// * input of 5, 2 → "no"
// * input of 5, 5 → "maybe"

```cpp
#include <string>
using std::string;

/**
 *  You and your date are trying to get a table at a 
 *  restaurant. The first input ("you") is the stylishness 
 *  of your clothes, in the range 0..10, and the second 
 *  ("date") is the stylishness of your date's clothes. 
 *  The result getting the table is encoded as "no", 
 *  "maybe", or "yes". If either of you is very stylish, 
 *  8 or more, then the result is yes. With the exception 
 *  that if either of you has style of 2 or less, then 
 *  the result is no. Otherwise the result is maybe. 
 */
string make_reservation(int you, int date)
{
    string reservation;
     // Add your code here
     if (you <= 2 || date <= 2) { reservation = "no"; }
     else if (you >= 8 || date >= 8)  { reservation = "yes"; } 
     else  { reservation = "maybe"; }
    
    return reservation;
}
```

/*

Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|make_reservation|2, 10|"no"|"no"|
|pass|make_reservation|10, 2|"no"|"no"|
|pass|make_reservation|8, 6|"yes"|"yes"|
|pass|make_reservation|3, 8|"yes"|"yes"|

Score

4/4

\*/

// https://codecheck.io/files/23020919307s2gztsv7l6h6efi4zewt61wf