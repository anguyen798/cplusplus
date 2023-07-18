// Write a program to calculate the surface area (A) of a capsule with a radius r and a side length a, using the formula:
// $$V = \pi R^{2} \left(\frac{4}{3} r + a\right)$$
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
    const string assignment = "Capsule Area";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, a;

    cout << "Enter the radius of the capsule: ";
    cin >> r;

    cout << "Enter the side length of the capsule: ";
    cin >> a;

    double area = 2 * pi * r * (2 * r + a);

    cout << "Area: [" << area << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://replit.com