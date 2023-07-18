// A stadium is a circle of radius r that has been cut in half through the center and the 2 ends are then separated by a rectangle of height r and width (or side length) of a. Write a program to calculate the area (A) using this formula.
// $$A = \pi R^{2} + 2ra$$

```cpp
#include <iostream>
#include <cmath>
#include <iomanip>
#include <string>
using namespace std;

int main()
{
////////////////// PUT ONLY YOUR CODE BELOW //////////////////////
    const double pi = acos(-1.0);
    const string FIRST_NAME = "First";
    const string LAST_NAME = "Last";
    const string assignment = "Stadium Area";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, a;

    cout << "Enter the radius of the stadium: ";
    cin >> r;

    cout << "Enter the width (or side length) of the rectangle: ";
    cin >> a;

    double area = pi * pow(r, 2) + 2 * r * a;

    cout << "Area: [" << area << "]" << endl;

    return 0;
}

```

// https://replit.com