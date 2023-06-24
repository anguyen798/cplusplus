```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Stadium Area";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, a;

    cout << "Enter the radius of the stadium: ";
    cin >> r;

    cout << "Enter the width (or side length) of the rectangle: ";
    cin >> a;

    double area = pi * pow(r, 2) + 2 * r * a;

    cout << "Area: [" << area << "]" << endl;

    return 0;
}

```