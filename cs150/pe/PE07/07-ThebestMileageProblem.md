// Using the Car structure defined in the file, taken from the 2017 EPA testing results, write the function named bestMileage().

//The function takes one input parameter: a vector of Cars that represents the testing data. The vector is sorted by manufacturer, so all cars of a particular manufacturer are together in the vector. The function also has an output parameter, a vector of string that contains both the manufacturer and the model concatenated together, separated by a semicolon, like this: "BMW;430i Coupe"

// Each entry is the car with the best mileage from each manufacturer. The function returns the average mileage of the selected cars.
// vector\<string\> vMileage;
//  double average = bestMileage(vCars, vMileage);
// For the example above, vCars is the Input parameter

// For the example above, vMileage is the Output parameter Here is the Car structure.
// The structure (don't change these)
// struct Car {
//    string mfg, model;
//    int horsepower, cylinders;
//    double mpg;
// };


```cpp
#include <string>
#include <vector>
#include <cmath>
using namespace std;

// The structure
struct Car {
    string mfg, model;
    int horsepower, cylinders;
    double mpg;
};

// WRITE YOUR FUNCTION BELOW THIS LINE
double bestMileage(const vector<Car>& v, vector<string>& vMileage)
{
   double result;
   // Add your work here
   return result;
}
```

```text
Testers

Running Tester.cpp

pass pass pass pass pass pass pass pass

Testing for the Best Mileage problem
--------------------------------------------
bestMileage(vCars, vMileage): [Mitsubishi;MIRAGE, Nissan;ARMADA 2WD]
Expected: [Mitsubishi;MIRAGE, Nissan;ARMADA 2WD]
 Avg mpg: 31.1
Expected: 31.1

bestMileage(vCars, vMileage): [Honda;RLX, Hyundai;Accent]
Expected: [Honda;RLX, Hyundai;Accent]
 Avg mpg: 39.0
Expected: 39.0

bestMileage(vCars, vMileage): [Jeep;Renegade 4x2, Kia;Forte]
Expected: [Jeep;Renegade 4x2, Kia;Forte]
 Avg mpg: 38.1
Expected: 38.1

bestMileage(vCars, vMileage): [BMW;230i Convertible]
Expected: [BMW;230i Convertible]
 Avg mpg: 45.8
Expected: 45.8

Score

8/8
```

https://codecheck.io/files/23041120442fw4urisfc3tn5xrtwwolpdf8