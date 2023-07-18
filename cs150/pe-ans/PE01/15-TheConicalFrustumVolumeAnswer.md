// Write a program to calculate the volume (V) of a conical frustum with a height h and the two radius r1 and r2. Here is the formula:
// $$V = \frac{1}{3} \pi h(r_{1}^{2} + r_{2}^{2} + r_{1} r_{2})$$
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
    const string assignment = "Conical Frustrum Volume";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double h, r1, r2;

    cout << "Enter the height of the conical frustum: ";
    cin >> h;
    cout << "Enter the radius of the larger base (r1): ";
    cin >> r1;
    cout << "Enter the radius of the smaller base (r2): ";
    cin >> r2;

    double volume = (1.0 / 3.0) * pi * h * (r1 * r1 + r2 * r2 + r1 * r2);

    cout << "Volume: [" << volume << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://replit.com