// Using the Star structure defined in the file, write the function named longestHop().

// The function takes one input parameter: a vector of Stars that represents a "travel itinerary". Visit every pair of stars in-order (0-1, 1-2, 2-3, etc.) and measure the distance between them. The function should return a vector of Star containing the two stars that are represent the longest "hop" or span between two stars in the trip.

// We'll assume that the stars are in 2D space and that you measure the distance using this formula.

// You may write a function to do so.
// d = sqrt ( (x2 - x1) ^ 2 + (y2 - y1) ^ 2 )
// vector\<Star\> longest = longestHop(vStars);

```cpp
#include <string>
#include <vector>
#include <cmath>
using namespace std;

// The structures
struct Star {
    double x, y;
    double magnitude;
    int draper;
    string names;
};


// WRITE YOUR FUNCTION BELOW THIS LINE

vector<Star> longestHop(const vector<Star>& v)
{
   vector<Star> result(2);
   // Add your work here
   return result;
}
```

/*
```text
Testers

Running Tester.cpp

pass pass pass

Testing for the Longest Hop problem
--------------------------------------------

  --longestHop(['ALPHERATZ', 'CAPH; CAS BETA'])->

 Longest: ['ALPHERATZ', 'CAPH; CAS BETA']
Expected: ['ALPHERATZ', 'CAPH; CAS BETA']

  --longestHop(['ALPHERATZ', 'CAPH; CAS BETA', 'ALGENIB'])->

 Longest: ['CAPH; CAS BETA', 'ALGENIB']
Expected: ['CAPH; CAS BETA', 'ALGENIB']

  --longestHop(['ALPHERATZ', 'CAPH; CAS BETA', 'ALGENIB', 'ANKAA'])->

 Longest: ['CAPH; CAS BETA', 'ALGENIB']
Expected: ['CAPH; CAS BETA', 'ALGENIB']

Score

3/3
```
\*/

// https://codecheck.io/files/23041120181i0k6pu5ggdpkbbg1s5s2avy9