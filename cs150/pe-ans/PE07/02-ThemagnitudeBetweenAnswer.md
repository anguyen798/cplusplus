// Using the Star structure defined in the file, write the function named magnitudeBetween().

// The function takes three input parameters: a vector of Stars as well as a lower and upper bounds. The function returns a vector of int containing Draper number of the stars whose magnitude falls between the two bounds (exclusive).

// vector\<size_t\> indexes;
// indexes = magnitudeBetween(vStars, 1.5, 3.4);

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

vector<int> magnitudeBetween(const vector<Star>& v, double lower, double upper)
{
   vector<int> result;
   // Iterate over each Star in the vector
   for (const auto & star: v)
   {
      // Check if the star's magnitude falls between the two bounds
      if (star.magnitude > lower && star.magnitude < upper) { result.push_back(star.draper); }
         // If it does, add the draper number to the result vector
   }
   
   return result;
}
```

/*
```text
Testers

Running Tester.cpp

pass pass pass pass

Testing for Magnitude Between problem
--------------------------------------------
magnitudeBetween(vStars, 0.50, 0.75): []
Expected: []

magnitudeBetween(vStars, 0.75, 1.00): [29139, 108248, 116658, 187642]
Expected: [29139, 108248, 116658, 187642]

magnitudeBetween(vStars, 1.00, 1.25): [62509, 148478, 216956]
Expected: [62509, 148478, 216956]

magnitudeBetween(vStars, 1.25, 1.50): [87901]
Expected: [87901]

Score

4/4
```
\*/

// https://codecheck.io/files/23041119566pt2ng82021kzk6wwxf1vdpum