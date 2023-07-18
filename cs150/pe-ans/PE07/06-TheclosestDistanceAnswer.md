// Using the Star structure defined in the file, write the function named closestDistance().

// The function takes one input parameter: a vector of Stars that represents a "travel itinerary". Visit every pair of stars in-order (0-1, 1-2, 2-3, etc.) and measure the distance between them. The function should return a vector of Star containing the two stars that are closest to each other in the trip.

// We'll assume that the stars are in 3D space and that you measure the distance using this formula.

// You may write a function to do so.
// d = sqrt( (x2 - x1)^2 + (y2 - y1) ^ 2) + (z2 - z1)^2 )
// vector\<Star\> closest = closestDistance(vStars);

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

// Function to calculate the distance between two stars
double distance(const Star& star1, const Star& star2)
{
   return sqrt(pow(star2.x - star1.x, 2) + pow(star2.y - star1.y, 2));
}

vector<Star> closestDistance(const vector<Star>& v)
{
   size_t len {v.size()};
   
   // if there's less than 2 stars in the vector, return the vector itself
   if(len < 2) { return v; }
   
   double minDist {distance(v.at(0), v.at(1))};
   vector<Star> closestStars = {v.at(0), v.at(1)};
   
   // iterate over each pair of stars
   for(size_t i {0}; i < len - 1; ++i)
   {
        double dist {distance(v.at(i), v.at(i + 1))};
        if(dist < minDist)
        {
            minDist = dist;
            closestStars.at(0) = v.at(i);
            closestStars.at(1) = v.at(i + 1);
        }
    }

    return closestStars;
}
```

/*
```text
Testers

Running Tester.cpp

pass pass pass

Testing for the Closest Distance problem
--------------------------------------------

  --closestDistance(['ALPHERATZ', 'CAPH; CAS BETA', 'ALGENIB'])->

 Closest: ['ALPHERATZ', 'CAPH; CAS BETA']
Expected: ['ALPHERATZ', 'CAPH; CAS BETA']

  --closestDistance(['ALPHERATZ', 'CAPH; CAS BETA', 'ALGENIB', 'ANKAA'])->

 Closest: ['ALGENIB', 'ANKAA']
Expected: ['ALGENIB', 'ANKAA']

  --closestDistance(['ALPHERATZ', 'CAPH; CAS BETA', 'ALGENIB', 'ANKAA', 'CAS LAMBDA', 'CAS KAPPA'])->

 Closest: ['CAS LAMBDA', 'CAS KAPPA']
Expected: ['CAS LAMBDA', 'CAS KAPPA']

Score

3/3
```
\*/

// https://codecheck.io/files/2304112032any5qn93stqia2wi2nstmn6db