```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Hemisphere Surface Area";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r;

    cout << "Enter the radius of the hemisphere (r): ";
    cin >> r;

    double surfaceArea = 3.0 * pi * pow(r, 2);

    cout << "Surface Area: [" << surfaceArea << "]" << endl;

    return 0;
}

```