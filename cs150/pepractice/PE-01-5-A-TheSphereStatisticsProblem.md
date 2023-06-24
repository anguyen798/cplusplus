```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Sphere Calculator";

    cout << STUDENT << ": ";
    cout << assignment << endl;
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