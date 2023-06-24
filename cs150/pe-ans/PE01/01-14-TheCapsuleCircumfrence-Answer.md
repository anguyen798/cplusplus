```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Capsule Circumference";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r;

    cout << "Enter the radius of the capsule: ";
    cin >> r;

    double circumference = 2 * pi * r;

    cout << "Circumference: [" << circumference << "]" << endl;

    return 0;
}

```