```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Cone Slant Height";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double r, h;

    cout << "Enter the radius of the cone: ";
    cin >> r;

    cout << "Enter the height of the cone: ";
    cin >> h;

    double slantHeight = sqrt(pow(h, 2) + pow(r, 2));

    cout << "Slant Height: [" << slantHeight << "]" << endl;

    return 0;
}

```