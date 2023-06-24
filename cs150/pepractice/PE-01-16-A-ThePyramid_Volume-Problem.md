```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Pyramid Volume";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double a, h;

    cout << "Enter the length of the base side (a): ";
    cin >> a;
    cout << "Enter the height of the pyramid (h): ";
    cin >> h;

    double volume = (1.0 / 3.0) * a * a * h;

    cout << "Volume: [" << volume << "]" << endl;

    return 0;
}

```