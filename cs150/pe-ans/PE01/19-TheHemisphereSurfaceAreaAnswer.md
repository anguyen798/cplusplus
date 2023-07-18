// Write a program to calculate the total surface area (K) of a hemisphere as shown here. Here is the formula:
// $$K = 3\pi r^{2}$$
```cpp
#include <iostream>
#include <cmath>
#include <iomanip>
#include <string>
using namespace std;

int main()
{
////////////////// PUT ONLY YOUR CODE BELOW //////////////////////
    // Add your code here
    const double pi = acos(-1.0);
    const string FIRST_NAME = "First";
    const string LAST_NAME = "Last";
    const string assignment = "Hemisphere Surface Area";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r;

    cout << "Enter the radius of the hemisphere (r): ";
    cin >> r;

    double surfaceArea = 3.0 * pi * pow(r, 2);

    cout << "Surface Area: [" << surfaceArea << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://replit.com