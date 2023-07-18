// Using the Star structure defined in the file, write the function named findStars().

// The function takes two input parameters: a vector of Stars and a string representing a star name or part of a star name. The function returns a vector of int representing the Draper numbers of the stars where the name was found. Use string::find() to search the star names. Remember that string::find() return string::npos when the search parameter is not found.

// vector\<int\> numbers;
// numbers = findStars(vStars, "VEG");

```cpp
#include <string>
#include <vector>
using namespace std;

// The structure
struct Star {
    double x, y;
    double magnitude;
    int draper;
    string names;
};

//WRITE YOUR FUNCTION BELOW THIS LINE

vector<int> findStars(const vector<Star>& v, const string& name)
{
   ... result;
   // Add your work here
   return result;
}
```

/*
```text
Testers

Running Tester.cpp

pass pass pass

Testing for Find Stars problem
--------------------------------------------
findStars(vec, "BETA"): [95418, 103192, 131873, 133208, 174638, 183912, 183914]
Expected: [95418, 103192, 131873, 133208, 174638, 183912, 183914]

findStars(vec, "XI"): [98230, 98231, 100407, 131156]
Expected: [98230, 98231, 100407, 131156]

findStars(vec, "MU"): [89758, 90432, 121370, 137391, 137392, 169702]
Expected: [89758, 90432, 121370, 137391, 137392, 169702]

Score

3/3
```
\*/

// https://codecheck.io/files/2304111951f5kmflo5yv5y4lbeghsshhxz0