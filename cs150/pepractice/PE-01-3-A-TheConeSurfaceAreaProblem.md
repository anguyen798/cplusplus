```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Cone Surface Area Calculator";

    cout << STUDENT << ": ";
    cout << assignment << endl;
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