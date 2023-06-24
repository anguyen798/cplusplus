```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Capsule Volume";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, a;

    cout << "Enter the radius of the capsule: ";
    cin >> r;

    cout << "Enter the side length of the capsule: ";
    cin >> a;

    double volume = pi * r * r * (4.0 / 3.0 * r + a);

    cout << "Volume: [" << volume << "]" << endl;

    return 0;
}

```