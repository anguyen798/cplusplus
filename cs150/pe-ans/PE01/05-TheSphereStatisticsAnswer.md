// Write a program to calculate both the volume and the area of a
sphere, given a radius r. The volume V, and the area A, are calculated
by using the formulas:
// $$V = \frac{4}{3} \pi r^{3}$$

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
    const string assignment = "Sphere Calculator";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << "\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\\\"" << endl;
    cout << endl;

    double radius;

    cout << "Enter the radius of the sphere: ";
    cin >> radius;

    double volume = (4.0 / 3.0) * pi * pow(radius, 3);
    double area = 4.0 * pi * pow(radius, 2);

    cout << "Volume: [" << volume << "]" << endl;
    cout << "Surface Area: [" << area << "]" << endl;

    return 0;
}

```

// https://codecheck.io/files/2305232053khpee41y69pz4s4iw1mrfu1j