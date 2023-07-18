// Write a program to calculate the total surface area of a right-circular code, like the one pictured here. To calculate the area (A) of a cone, given a radius (r) and a height (h), the formula is:
// $$A = \pi r (r + \sqrt{h^{2} + r^{2}})$$

```cpp
#include <iostream>
#include <cmath>
#include <iomanip>
#include <string>
using namespace std;

int main()
{
    using namespace std;

    const double pi = acos(-1.0);
    const string FIRST_NAME = "First";
    const string LAST_NAME = "Last";
    const string assignment = "Cone Surface Area Calculator";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << "\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\\\"" << endl;
    cout << endl;

    double radius, height;

    cout << "Enter the radius of the cone: ";
    cin >> radius;

    cout << "Enter the height of the cone: ";
    cin >> height;

    double surfaceArea = pi * radius * (radius + sqrt(pow(height, 2) + pow(radius, 2)));

    cout << "Surface Area: [" << surfaceArea << "]" << endl;

    return 0;
}

```

// https://codecheck.io/files/23052320457sjoudc7a7f096sj076bszujx