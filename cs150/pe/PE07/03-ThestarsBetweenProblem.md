// Using the Star structure defined in the file. Write the function named starsBetween().

// The function takes three input parameters: a vector of Star s as well as a lower and upper bounds for the magnitude of the star. The function returns a double representing the average magnitude of the stars falling between the two bounds (exclusive). If no stars are in the range, then return -1. In addition, the function has an output parameter that returns the names of the stars that are included.

// vector\<string\> names;
// double avg = starsBetween(vStars, names, 2.3, 2.4);
// For the above vStars is the Input parameter.
// For the above names is the Output parameter.

```cpp
#include <string>
#include <vector>
#include <cmath>
using namespace std;

// The structure
struct Star {
    double x, y;
    double magnitude;
    int draper;
    string names;
};

// WRITE YOUR FUNCTION BELOW THIS LINE

double starsBetween(const vector<Star>& v, vector<string>& names, double lower, double upper)
{
   double result;
   // Add your work here
   return result;
}
```

/*
```text
Testers

Running Tester.cpp

pass pass pass pass pass pass

Testing for the Stars Between problem
--------------------------------------------
starsBetween(vStars, names, 1.43, 1.53)-> 
   Names: [ADHARA]
Expected: [ADHARA]
 Average: 1.50
Expected: 1.50

starsBetween(vStars, names, 1.83, 1.93)-> 
   Names: [MENKALINAN, ALHENA; GEM GAMMA, AVIOR, ALKAID; UMA ETA; BENETNASCH, ATRIA]
Expected: [MENKALINAN, ALHENA; GEM GAMMA, AVIOR, ALKAID; UMA ETA; BENETNASCH, ATRIA]
 Average: 1.89
Expected: 1.89

starsBetween(vStars, names, 2.23, 2.33)-> 
   Names: [CAPH; CAS BETA, SCHEDAR; CAS ALPHA, MINTAKA; ORI DELTA, ELTANIN]
Expected: [CAPH; CAS BETA, SCHEDAR; CAS ALPHA, MINTAKA; ORI DELTA, ELTANIN]
 Average: 2.25
Expected: 2.25

Score

6/6
```

\*/

// https://codecheck.io/files/23041120004pjg1t35hfxifox37w103u1so