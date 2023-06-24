```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Conical Frustrum Volume";

    cout << STUDENT << ": ";
    cout << assignment << endl;
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

    return 0;
}

```