// Write a program to calculate the slant height (S) of a right-circular code, like the one pictured here. Given a radius (r) and a height (h), the formula is:
// $$S = \sqrt{h^{2} + r^{2}}$$

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
    const string assignment = "Cone Slant Height";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, h;

    cout << "Enter the radius of the cone: ";
    cin >> r;

    cout << "Enter the height of the cone: ";
    cin >> h;

    double slantHeight = sqrt(pow(h, 2) + pow(r, 2));

    cout << "Slant Height: [" << slantHeight << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}

```

// https://replit.com