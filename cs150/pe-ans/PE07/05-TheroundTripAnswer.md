// Using the Star structure defined in the file, write the function named roundTrip().

// The function takes one input parameter: a vector of Stars that represents a "travel itinerary". Visit every pair of stars in-order (0-1, 1-2, 2-3, etc.) and add up the distance between them. When you reach the last star, include in your sum the distance between it and the first. The function returns the round-trip distance as a double. The function also has one output parameter that returns the average magnitude of all of the stars visited.

// We'll assume that the stars are in 2D space and that you measure the distance using this formula.

// You may write a function to do so.
// d = sqrt ( (x2 - x1) ^ 2 + (y2 - y1) ^ 2 )
// double average;
// double distance = roundTrip(vStars, average);
// For the above example, vStars is the Input parameter
// For the above example, average is the Output parameter

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

// Function to calculate the distance between two stars
double distance(const Star& star1, const Star& star2)
{
   return sqrt(pow(star2.x - star1.x, 2) + pow(star2.y - star1.y, 2));
}

double roundTrip(const vector<Star>& v, double& avgMagnitude)
{
   double totalDistance {0.0}, totalMagnitude {0.0};
   size_t len {v.size()};

   // If the vector is empty, there's no magnitude to calculate.
   if (len == 0) {
       avgMagnitude = 0.0;
       return totalDistance;
   }

   // Iterate over each Star in the vector
   for (size_t i {0}; i < len; ++i)
   {
      // Add the star's magnitude to the total
      totalMagnitude += v.at(i).magnitude;
      
      // If it's not the last star, add the distance to the next star to the total distance
      if (i < len - 1) { totalDistance += distance(v.at(i), v.at(i + 1)); }
      
      // If it is the last star, add the distance to the first star
      else { totalDistance += distance(v.at(i), v.at(0)); }
   }

   // Calculate the average magnitude
   avgMagnitude = totalMagnitude / len;

   return totalDistance;
}
```

/*
```text
Testers

Running Tester.cpp

pass pass pass pass pass pass

Testing for Round Trip problem
--------------------------------------------
roundTrip([], avgMag)->
 distance: 0
Expected: 0
Avg magnitude: 0
Expected: 0

roundTrip([(ORI THETA:6.71), (ORI THETA:4.98), (ORI IOTA:2.75), (ALNILAM; ORI EPSILON:1.69)], avgMag)->
 distance: 0.0132398
Expected: 0.0132398
Avg magnitude: 4.0325
Expected: 4.0325

roundTrip([(CAPH; CAS BETA:2.28), (ALGENIB:2.83), (ANKAA:2.40), (CAS LAMBDA:4.74), (CAS KAPPA:4.17)], avgMag)->
 distance: 1.0449
Expected: 1.0449
Avg magnitude: 3.284
Expected: 3.284

Score

6/6
```
\*/

// https://codecheck.io/files/2304112024cx7bc3th71t6sivsz69gkw55i