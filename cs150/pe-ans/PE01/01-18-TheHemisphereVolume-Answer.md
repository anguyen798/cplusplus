```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Hemisphere Volume";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r;

    cout << "Enter the radius of the hemisphere (r): ";
    cin >> r;

    double volume = (2.0 / 3.0) * pi * pow(r, 3);

    cout << "Volume: [" << volume << "]" << endl;

    return 0;
}

```