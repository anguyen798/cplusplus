// Write a program to calculate the circumference (C) of a capsule with a radius r and a side length a, using the formula:
// $$C = 2 \pi r$$
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
    const string assignment = "Capsule Circumference";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r;

    cout << "Enter the radius of the capsule: ";
    cin >> r;

    double circumference = 2 * pi * r;

    cout << "Circumference: [" << circumference << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://replit.com