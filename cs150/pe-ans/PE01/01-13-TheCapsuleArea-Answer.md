```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Capsule Area";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, a;

    cout << "Enter the radius of the capsule: ";
    cin >> r;

    cout << "Enter the side length of the capsule: ";
    cin >> a;

    double area = 2 * pi * r * (2 * r + a);

    cout << "Area: [" << area << "]" << endl;

    return 0;
}

```