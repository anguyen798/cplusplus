// We are having a party with amounts of tea and candy. Print the outcome of the party as "bad", "good" or "great". A party is good if both tea and candy are at least 5. However, if either tea or candy is at least double the amount of the other one, the party is great. However, in all cases, if either tea or candy is less than 5, the party is always bad.

// * input of 6, 8 → "good"
// * input of 3, 8 → "bad"
// * input of 20, 6 → "great"

```cpp
#include <string>
using namespace std;
/**
 *  We are having a party with amounts of tea and candy. 
 *  Set the outcome of the party as "bad", "good" or "great". 
 *  A party is good if both tea and candy are at least 5. 
 *  However, if either tea or candy is at least double 
 *  the amount of the other one, the party is great. 
 *  However, in all cases, if either tea or candy is less 
 *  than 5, the party is always bad. 
 */
string tea_party(int tea, int candy)
{
    string outcome;
   
    // ---- YOUR CODE GOES ONLY BELOW THIS LINE
  // Add your code here
  // Check if either tea or candy is less than 5
  if (tea < 5 || candy < 5) { outcome = "bad"; }
  
  // Then check if either is at least double the other
  else if (tea >= 2 * candy || candy >= 2 * tea) { outcome = "great"; } 
  
  // If neither condition is met, the party is good
  else { outcome = "good"; }

   return outcome;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|tea_party|6, 8|"good"|"good"|
|pass|tea_party|3, 8|"bad"|"bad"|
|pass|tea_party|20, 6|"great"|"great"|

Score

3/3
\*/

// https://codecheck.io/files/23020821337xwuhu2u80pri25f1blesqak2