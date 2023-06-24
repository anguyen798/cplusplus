```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Pyramid Surface Area";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double a, h;

    cout << "Enter the length of the base side (a): ";
    cin >> a;
    cout << "Enter the height of the pyramid (h): ";
    cin >> h;

    double surfaceArea = a * (a + sqrt(a * a + 4 * h * h));

    cout << "Surface Area: [" << surfaceArea << "]" << endl;

    return 0;
}

```